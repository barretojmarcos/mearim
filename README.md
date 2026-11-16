# Rio Mearim — site público

Este repositório publica o painel do nível do Rio Mearim (estação Pedreiras II, ANA 33281000) e o telão da 13ª CIBM.

- O ramo `main` tem só o agendamento (`.github/workflows/atualizar.yml`) e este arquivo. Um relógio externo (cron-job.org) dispara o workflow às :07, :22, :37 e :52, e o agendamento do GitHub nos mesmos minutos fica de reserva. O site é montado uma vez por hora e, com a vigília ligada (rio a partir de 4,50 m), a cada 15 minutos.
- O ramo `dados` guarda as medições em CSV mensais, o histórico das 07h, a cópia da planilha e a hora da última execução completa. **É gravado por máquina a cada execução; não edite à mão.**
- O código que coleta e monta o site fica em outro repositório, privado.

As medições são dados públicos da Agência Nacional de Águas (ANA).

Segredos do repositório: `ANA_USER`, `ANA_PASSWORD`, `CODIGO_DEPLOY_KEY`, `TELEGRAM_BOT_TOKEN`, `TELEGRAM_CHAT_ID` e, opcional, `HEALTHCHECK_URL`. O passo a passo está no guia de operação.
