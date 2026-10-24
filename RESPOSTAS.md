Respostas das Atividades - Bento Ramalho Botelho

 1- No TDD, retornar um valor fixo é aceitável no primeiro ciclo para garantir que a estrutura do teste e da classe esteja funcionando e ver o teste passar o mais rápido possível. O que obrigou a escrever a soma real foi o Ciclo 2 (Triangulação), onde a adição de um segundo caso de teste com entradas e resultados diferentes fez o valor fixo falhar, forçando a implementação do algoritmo real.

 2- Trata-se da técnica de "Análise do Valor Limite". O ponto exato de mudança de comportamento da regra de negócio é o 70 (aprovado) e o 69 (reprovado). Testar com 50 e 90 não garante que a lógica de comparação esteja correta (como usar `>= 70` em vez de `> 70`), enquanto testar exatamente nos limites valida a precisão da condicional.

 3. No Ciclo 4, o que mudou na refatoração? Como você teve certeza de que não quebrou nada?
Na refatoração, eliminamos a duplicação de código criando um método privado auxiliar para isolar as regras de validação das notas. A certeza de que nada foi quebrado veio da "suíte de testes automatizados": após a alteração do código, rodamos todos os testes novamente e eles continuaram 100% verdes.

 4. No Ciclo 8, por que alteramos os testes antes de mudar o código?
Porque no TDD os testes funcionam como a "especificação executável" das regras de negócio. Quando os requisitos mudam, primeiro atualizamos os testes para refletir a nova regra, e só então alteramos o código de produção para satisfazer a nova especificação.

 5. Qual ciclo foi o mais difícil para você, e por quê?
O pior foi o ciclo 2, pois foi o início antes de pegar o embalo para você fazer os outros, tanto que muitas vezes para rodar os testes estavam falhando, então tive que pedir muita ajuda para o professor, mas quando domina esse ciclo todos os outros ficam mais fáceis