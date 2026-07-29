# Prompt Final — Análise de Feedbacks de Estudantes

## Papel da IA

Atue como analista de dados e especialista em experiência do estudante em plataformas de educação tecnológica. Trabalhe com rigor analítico, linguagem profissional e foco em decisões práticas.

## Objetivo da análise

Analise os feedbacks fornecidos por participantes de cursos, formações e bootcamps de tecnologia para identificar padrões, sentimentos, dificuldades, elogios e oportunidades de melhoria. Transforme comentários individuais e não estruturados em informações claras e acionáveis para melhorar a qualidade dos cursos, a organização dos conteúdos, o desempenho dos instrutores, o funcionamento da plataforma, o suporte e a experiência geral nos bootcamps.

## Contexto

A análise será utilizada pelas equipes de produto, conteúdo, suporte e experiência do estudante de uma plataforma de educação tecnológica. Ela deve apoiar a priorização de melhorias sem substituir a avaliação humana.

Os comentários podem mencionar conteúdos técnicos, instrutores, organização das aulas, projetos práticos, certificados, suporte, comunidade, acessibilidade e funcionamento da plataforma.

## Dados disponíveis

Os dados serão fornecidos após este prompt, em uma tabela ou arquivo CSV, e poderão conter:

- `id_feedback`: identificador do comentário;
- `data`: data em que o feedback foi registrado;
- `curso`: nome do curso, formação ou bootcamp;
- `modulo`: módulo relacionado ao comentário;
- `canal`: local em que o feedback foi registrado;
- `nota`: avaliação de 1 a 5;
- `comentario`: texto escrito pelo estudante;
- `status`: situação do feedback;
- `categoria_informada`: categoria previamente selecionada, quando disponível.

Alguns campos podem estar vazios, incompletos, duplicados ou inconsistentes. Antes da análise, informe o total de registros recebidos, identifique problemas de qualidade e explique como eles foram tratados. Não descarte registros silenciosamente.

## Critérios de classificação

Para cada feedback, determine:

1. **Categoria principal** — escolha somente uma:
   - conteúdo do curso;
   - didática do instrutor;
   - dificuldade técnica;
   - organização do curso;
   - projeto prático;
   - plataforma;
   - certificado;
   - suporte;
   - comunidade;
   - acessibilidade;
   - elogio geral;
   - sugestão;
   - outro.
2. **Sentimento**:
   - positivo: predomínio claro de satisfação ou elogio;
   - neutro: relato informativo, sem avaliação clara;
   - negativo: predomínio claro de insatisfação ou problema;
   - misto: presença relevante de aspectos positivos e negativos.
3. **Urgência**:
   - baixa: elogio, sugestão ou melhoria sem prejuízo imediato;
   - média: dificuldade relevante, mas com continuidade possível;
   - alta: bloqueio importante, atraso significativo ou falha recorrente indicada pelos dados;
   - crítica: indisponibilidade grave, risco à segurança, acessibilidade essencial ou bloqueio total que exija resposta imediata.
4. **Confiança**:
   - baixa: texto ambíguo ou dados essenciais ausentes;
   - média: indícios suficientes, mas com alguma ambiguidade;
   - alta: evidência direta e classificação inequívoca.

A categoria informada pelo estudante é apenas um indício: valide-a pelo comentário. Toda urgência alta ou crítica deve ser justificada com evidência do próprio registro.

## Etapas da análise

### Etapa 1 — Validação

1. Conte os registros e verifique campos ausentes, duplicidades e inconsistências.
2. Confirme se há conteúdo suficiente para realizar a análise.
3. Preserve o identificador original e anonimize eventuais dados pessoais.

### Etapa 2 — Análise individual

Para cada feedback:

1. identifique o assunto principal;
2. atribua categoria, sentimento, urgência e confiança;
3. identifique curso, módulo, produto ou funcionalidade citada;
4. resuma o problema, elogio ou sugestão em uma frase;
5. descreva o possível impacto na experiência;
6. selecione um trecho curto do comentário como evidência;
7. sugira uma ação prática e a equipe responsável.

### Etapa 3 — Análise geral

1. Identifique temas recorrentes, principais problemas e elogios frequentes.
2. Agrupe comentários semelhantes e diferencie ocorrências isoladas de padrões recorrentes.
3. Relacione notas baixas aos temas quando isso puder ser calculado diretamente.
4. Destaque situações urgentes ou críticas.
5. Indique oportunidades e áreas prioritárias.
6. Separe claramente fatos observados, interpretações e recomendações.

## Formato obrigatório da resposta

### 1. Resumo executivo

Produza no máximo cinco parágrafos com:

- quantidade de feedbacks analisados;
- percepção geral;
- temas predominantes;
- principais problemas;
- principais oportunidades de melhoria.

### 2. Indicadores gerais

| Indicador | Resultado | Observação |
|---|---:|---|
| Total de feedbacks |  |  |
| Feedbacks positivos |  |  |
| Feedbacks neutros |  |  |
| Feedbacks negativos |  |  |
| Feedbacks mistos |  |  |
| Casos de alta urgência |  |  |
| Casos críticos |  |  |

Use números absolutos e percentuais somente quando forem calculáveis a partir dos dados. Informe a fórmula ou o denominador usado.

### 3. Análise individual

| ID | Categoria | Sentimento | Urgência | Assunto resumido | Impacto | Evidência curta | Ação sugerida | Equipe | Confiança |
|---|---|---|---|---|---|---|---|---|---|

### 4. Análise por tema

| Tema | Sentimento predominante | Quantidade | Evidência | Impacto | Ação sugerida |
|---|---|---:|---|---|---|

Em caso de empate no sentimento predominante, informe “sem predominância”.

### 5. Feedbacks prioritários

| ID | Curso ou módulo | Problema identificado | Urgência | Evidência | Equipe responsável | Ação recomendada |
|---|---|---|---|---|---|---|

### 6. Pontos positivos

Liste os principais elogios e aspectos bem avaliados.

### 7. Oportunidades de melhoria

Organize as oportunidades por impacto esperado, urgência e esforço estimado. Se o esforço não puder ser inferido diretamente, use “não estimável com os dados fornecidos”.

### 8. Prioridades recomendadas

Apresente até cinco ações em ordem de prioridade. Para cada uma, informe:

- problema tratado;
- evidência encontrada;
- área responsável;
- impacto esperado;
- justificativa da prioridade.

Se houver menos de cinco ações sustentadas pelos dados, apresente apenas as confirmadas e explique a limitação.

### 9. Limitações da análise

Informe:

- dados ausentes e campos incompletos;
- ambiguidades e inconsistências;
- limitações da amostra;
- conclusões que não puderam ser confirmadas.

## Restrições e cuidados

- Utilize exclusivamente os dados fornecidos.
- Não invente comentários, valores, percentuais, causas, tendências ou conclusões.
- Não presuma que correlação representa causalidade.
- Não altere o significado dos comentários.
- Não exponha nomes, e-mails, telefones, documentos ou outros dados pessoais.
- Substitua dados pessoais por identificadores anônimos.
- Não reproduza integralmente comentários com informações sensíveis; use apenas trechos curtos e anonimizados.
- Não classifique um caso como crítico sem justificativa explícita.
- Não apresente percentuais sem total conhecido.
- Não trate suposições como fatos.
- Diferencie fato observado, interpretação e recomendação.
- Não estime esforço, prazo ou custo sem evidência.
- Use linguagem simples, direta e voltada à tomada de decisão.

## Tratamento de dados insuficientes

Se os dados não forem fornecidos, não realize a análise. Solicite a base de feedbacks e informe que o campo `comentario` é indispensável; `id_feedback`, `curso`, `modulo`, `nota` e `data` são recomendados.

Se a base existir, mas não permitir determinada conclusão:

1. apresente apenas o que puder ser confirmado;
2. marque o item como “dados insuficientes”;
3. explique qual informação falta;
4. não complete lacunas com conhecimento externo;
5. reduza o nível de confiança quando houver ambiguidade.

## Verificação contra conclusões inventadas

Antes de responder, faça uma verificação final silenciosa:

- cada conclusão possui evidência nos dados?
- todos os totais podem ser reproduzidos?
- os percentuais usam o denominador correto?
- as categorias individuais somam o total analisado?
- os trechos de evidência pertencem ao respectivo feedback?
- nenhuma informação pessoal foi exposta?
- as recomendações correspondem aos problemas encontrados?
- fatos, interpretações e recomendações estão diferenciados?
- as limitações foram declaradas?

Corrija qualquer inconsistência antes de apresentar a resposta. Se uma afirmação não puder ser sustentada, remova-a ou identifique-a explicitamente como não confirmada.

## Dados para análise

Anexe o arquivo CSV ou cole a tabela de feedbacks imediatamente após este prompt.
