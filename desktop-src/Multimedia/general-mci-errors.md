---
title: Erros gerais de MCI
description: Erros gerais de MCI
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- Valores de retorno do MCIERR, erros gerais
- referência multimídia, erros de MCI
- referência para multimídia, erros de MCI
- MCI (Interface de Controle de Mídia), erros gerais
- MCI (Interface de Controle de Mídia), erros gerais
- referência para MCI, erros gerais
- Referência de MCI, erros gerais
- MCI (Interface de Controle de Mídia), erros
- MCI (Interface de Controle de Mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- Função mciSendCommand
- Função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f402e532f1bcf22a9136764647c91b1f4d54479f932c509ec172c1d973f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375153"
---
# <a name="general-mci-errors"></a>Erros gerais de MCI

Os seguintes valores de erro podem ser retornados pela [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) ou [**mciSendString:**](/previous-versions//dd757161(v=vs.85))



| Valor                            | Significado                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FORMATO DE HORA RUIM DO MCIERR \_ \_ \_        | O valor especificado para o formato de hora é inválido.                                                                                                         |
| O MCIERR \_ NÃO PODE CARREGAR O \_ \_ DRIVER     | O driver de dispositivo especificado não será carregado corretamente.                                                                                                         |
| O MCIERR \_ NÃO PODE \_ USAR \_ TODOS         | O nome do dispositivo "all" não é permitido para este comando.                                                                                                      |
| MCIERR \_ CREATEWINDOW             | Não foi possível criar ou usar a janela.                                                                                                                             |
| COMPRIMENTO DO DISPOSITIVO MCIERR \_ \_           | O nome do dispositivo ou driver é muito longo. Especifique um nome de dispositivo ou driver com menos de 79 caracteres.                                                     |
| DISPOSITIVO MCIERR \_ \_ BLOQUEADO           | O dispositivo agora está sendo fechado. Aguarde alguns segundos e tente novamente.                                                                                         |
| DISPOSITIVO MCIERR \_ \_ NÃO \_ INSTALADO   | O dispositivo especificado não está instalado no sistema. Use a opção Drivers do Painel de Controle para instalar o dispositivo.                                   |
| O DISPOSITIVO MCIERR \_ \_ NÃO ESTÁ \_ PRONTO       | O driver de dispositivo não está pronto.                                                                                                                             |
| DISPOSITIVO MCIERR \_ \_ ABERTO             | O nome do dispositivo já é usado como um alias por este aplicativo. Use um alias exclusivo.                                                                        |
| COMPRIMENTO DE \_ \_ ORD DO DISPOSITIVO MCIERR \_      | O nome do dispositivo ou driver é muito longo. Especifique um nome de dispositivo ou driver com menos de 79 caracteres.                                                     |
| TIPO DE DISPOSITIVO MCIERR \_ \_ \_ NECESSÁRIO   | O dispositivo especificado não pode ser encontrado no sistema. Verifique se o dispositivo está instalado e se o nome do dispositivo está escrito corretamente.                            |
| MCIERR \_ DRIVER                   | O driver de dispositivo exibe um problema. Verifique com o fabricante do dispositivo sobre como obter um novo driver.                                                      |
| DRIVER MCIERR \_ \_ INTERNO         | O driver de dispositivo exibe um problema. Verifique com o fabricante do dispositivo sobre como obter um novo driver.                                                      |
| ALIAS \_ DUPLICADO DO MCIERR \_         | O alias especificado já é usado neste aplicativo. Use um alias exclusivo.                                                                                |
| EXTENSÃO MCIERR \_ \_ NÃO \_ ENCONTRADA    | A extensão especificada não tem nenhum tipo de dispositivo associado a ela. Especifique um tipo de dispositivo.                                                                       |
| CARACTERES EXTRAS DO MCIERR \_ \_        | Você deve colocar uma cadeia de caracteres entre aspas; caracteres após as aspas de fechamento não são válidos.                                              |
| ARQUIVO MCIERR \_ \_ NÃO \_ ENCONTRADO         | O arquivo solicitado não foi encontrado. Verifique se o caminho e o nome do arquivo estão corretos.                                                                             |
| ARQUIVO MCIERR \_ \_ NÃO \_ SALVO         | O arquivo não foi salvo. Certifique-se de que seu sistema tenha espaço em disco suficiente ou tenha uma conexão de rede intacta.                                                |
| MCIERR \_ FILE \_ READ               | Falha na leitura do arquivo. Certifique-se de que o arquivo esteja presente no sistema ou se o sistema tem uma conexão de rede intacta.                             |
| GRAVAÇÃO DE \_ ARQUIVO MCIERR \_              | Falha na gravação no arquivo. Certifique-se de que seu sistema tenha espaço em disco suficiente ou tenha uma conexão de rede intacta.                                            |
| MCIERR \_ FILENAME \_ OBRIGATÓRIO       | O nome do arquivo é inválido. Certifique-se de que o nome do arquivo não tenha mais de oito caracteres, seguido por um ponto e uma extensão.                                  |
| SINALIZADORES MCIERR \_ \_ NÃO \_ COMPATÍVEIS   | Os parâmetros especificados não podem ser usados juntos.                                                                                                           |
| MCIERR \_ GET \_ CD                  | O arquivo solicitado ou dispositivo MCI não foi encontrado. Tente alterar diretórios ou reiniciar o sistema.                                                         |
| MCIERR \_ HARDWARE                 | O dispositivo especificado exibe um problema. Verifique se o dispositivo está funcionando corretamente ou entre em contato com o fabricante do dispositivo.                                     |
| MCIERR \_ ILEGAL PARA ABERTURA \_ \_ \_ AUTOMÁTICA | A MCI não executará o comando especificado em um dispositivo aberto automaticamente. Aguarde até que o dispositivo seja fechado e tente executar o comando.             |
| MCIERR \_ INTERNO                 | Ocorreu um problema ao inicializar a MCI. Tente reiniciar o sistema Windows sistema operacional.                                                                        |
| ID \_ DE DISPOSITIVO INVÁLIDA DO MCIERR \_ \_      | ID do dispositivo inválida. Use a ID dada ao dispositivo quando o dispositivo foi aberto.                                                                               |
| MCIERR \_ NOME DE DISPOSITIVO \_ \_ INVÁLIDO    | O dispositivo especificado não está aberto nem reconhecido pela MCI.                                                                                                     |
| ARQUIVO MCIERR \_ \_ INVÁLIDO            | O arquivo especificado não pode ser interpretado no dispositivo MCI especificado. O arquivo pode estar corrompido ou pode usar um formato de arquivo incorreto.                               |
| PARÂMETRO AUSENTE DO \_ MCIERR \_       | O comando especificado requer um parâmetro , que você deve fornecer.                                                                                          |
| MCIERR \_ MULTIPLE                 | Ocorreram erros em mais de um dispositivo. Especifique cada comando e dispositivo separadamente para identificar os dispositivos que estão causando os erros.                             |
| O MCIERR \_ DEVE \_ USAR \_ SHAREABLE     | O driver de dispositivo já está em uso. Você deve especificar o parâmetro "compartilhável" com cada comando aberto para compartilhar o dispositivo.                                  |
| MCIERR \_ SEM \_ ELEMENTO \_ PERMITIDO     | O dispositivo especificado não usa um nome de arquivo.                                                                                                               |
| MCIERR \_ SEM \_ INTEIRO              | O parâmetro para esse comando MCI deve ser um valor inteiro.                                                                                                |
| MCIERR \_ SEM \_ JANELA               | Não há nenhuma janela de exibição.                                                                                                                                 |
| FUNÇÃO MCIERR \_ NÃO \_ AAPPLICABLE  | A sequência de comandos MCI especificada não pode ser executada na ordem especificada. Corrigir a sequência de comandos; em seguida, tente novamente.                                   |
| BLOCO DE PARÂMETRO \_ \_ NULO MCIERR \_   | Um bloco de parâmetro nulo (estrutura) foi passado para a MCI.                                                                                                       |
| MCIERR \_ \_ SEM \_ MEMÓRIA          | Seu sistema não tem memória suficiente para essa tarefa. Saia de um ou mais aplicativos para aumentar a memória disponível e tente executar a tarefa novamente. |
| MCIERR \_ OUTOFRANGE               | O valor do parâmetro especificado está fora do intervalo para o comando MCI especificado.                                                                                |
| MCIERR \_ SET \_ CD                  | O arquivo especificado ou o dispositivo MCI está inacessível porque o aplicativo não pode alterar diretórios.                                                         |
| UNIDADE MCIERR \_ SET \_               | O arquivo especificado ou o dispositivo MCI está inacessível porque o aplicativo não pode alterar as unidades.                                                              |
| RECURSO SEM NOME \_ DO MCIERR \_        | Você não pode armazenar um arquivo sem nome. Especifique um nome de arquivo.                                                                                                       |
| COMANDO MCIERR \_ UNRECOGNIZED \_    | O driver não pode reconhecer o comando especificado.                                                                                                          |
| FUNÇÃO SEM \_ SUPORTE DO MCIERR \_    | O driver de dispositivo MCI que o sistema está usando não dá suporte ao comando especificado.                                                                           |



 

 

 