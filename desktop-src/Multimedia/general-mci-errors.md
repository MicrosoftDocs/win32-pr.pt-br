---
title: Erros gerais de MCI
description: Erros gerais de MCI
ms.assetid: be9c4a2b-44bc-410c-be74-ba55bb4e785b
keywords:
- MCIERR valores de retorno, erros gerais
- referência de multimídia, erros MCI
- referência para multimídia, erros MCI
- MCI (interface de controle de mídia), erros gerais
- MCI (interface de controle de mídia), erros gerais
- referência para MCI, erros gerais
- Referência de MCI, erros gerais
- MCI (interface de controle de mídia), erros
- MCI (interface de controle de mídia), erros
- referência para MCI, erros
- Referência de MCI, erros
- função mciSendCommand
- função mciSendString
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44538937be73c2ccfb1d30de1f1a1c729cc05095
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104293944"
---
# <a name="general-mci-errors"></a>Erros gerais de MCI

Os seguintes valores de erro podem ser retornados pela função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) ou [**mciSendString**](/previous-versions//dd757161(v=vs.85)) :



| Valor                            | Significado                                                                                                                                                     |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MCIERR \_ \_ formato de tempo inadequado \_        | O valor especificado para o formato de hora é inválido.                                                                                                         |
| MCIERR \_ não pode \_ carregar o \_ Driver     | O driver de dispositivo especificado não será carregado corretamente.                                                                                                         |
| MCIERR \_ não pode \_ usar \_ todos         | O nome do dispositivo "All" não é permitido para este comando.                                                                                                      |
| MCIERR \_ CREATEWINDOW             | Não foi possível criar ou usar a janela.                                                                                                                             |
| \_comprimento do dispositivo MCIERR \_           | O nome do dispositivo ou do driver é muito longo. Especifique um nome de dispositivo ou driver que tenha menos de 79 caracteres.                                                     |
| \_dispositivo MCIERR \_ bloqueado           | O dispositivo agora está sendo fechado. Aguarde alguns segundos e tente novamente.                                                                                         |
| \_dispositivo MCIERR \_ não \_ instalado   | O dispositivo especificado não está instalado no sistema. Use a opção drivers do painel de controle para instalar o dispositivo.                                   |
| o \_ dispositivo MCIERR \_ não \_ está pronto       | O driver do dispositivo não está pronto.                                                                                                                             |
| \_dispositivo MCIERR \_ aberto             | O nome do dispositivo já está sendo usado como um alias por este aplicativo. Use um alias exclusivo.                                                                        |
| \_comprimento de \_ Ord do dispositivo MCIERR \_      | O nome do dispositivo ou do driver é muito longo. Especifique um nome de dispositivo ou driver que tenha menos de 79 caracteres.                                                     |
| \_tipo de dispositivo MCIERR \_ \_ necessário   | O dispositivo especificado não foi encontrado no sistema. Verifique se o dispositivo está instalado e se o nome do dispositivo está escrito corretamente.                            |
| \_Driver MCIERR                   | O driver de dispositivo exibe um problema. Verifique com o fabricante do dispositivo sobre como obter um novo driver.                                                      |
| \_Driver MCIERR \_ interno         | O driver de dispositivo exibe um problema. Verifique com o fabricante do dispositivo sobre como obter um novo driver.                                                      |
| \_alias duplicado MCIERR \_         | O alias especificado já está em uso neste aplicativo. Use um alias exclusivo.                                                                                |
| \_extensão MCIERR \_ não \_ encontrada    | A extensão especificada não tem nenhum tipo de dispositivo associado a ela. Especifique um tipo de dispositivo.                                                                       |
| MCIERR \_ \_ caracteres extras        | Você deve colocar uma cadeia de caracteres entre aspas; os caracteres após a aspa de fechamento não são válidos.                                              |
| \_arquivo MCIERR \_ não \_ encontrado         | O arquivo solicitado não foi encontrado. Verifique se o caminho e o nome do arquivo estão corretos.                                                                             |
| \_arquivo MCIERR \_ não \_ salvo         | O arquivo não foi salvo. Verifique se o sistema tem espaço em disco suficiente ou se há uma conexão de rede intacta.                                                |
| \_leitura do arquivo MCIERR \_               | Falha na leitura do arquivo. Verifique se o arquivo está presente no sistema ou se o sistema tem uma conexão de rede intacta.                             |
| \_gravação de arquivo MCIERR \_              | Falha na gravação do arquivo. Verifique se o sistema tem espaço em disco suficiente ou se há uma conexão de rede intacta.                                            |
| \_nome de arquivo MCIERR \_ necessário       | O nome do arquivo é inválido. Verifique se o nome do arquivo não tem mais de oito caracteres, seguido de um ponto e uma extensão.                                  |
| \_sinalizadores MCIERR \_ não \_ compatíveis   | Os parâmetros especificados não podem ser usados juntos.                                                                                                           |
| MCIERR \_ obter \_ CD                  | O arquivo solicitado ou o dispositivo MCI não foi encontrado. Tente alterar os diretórios ou reiniciar o sistema.                                                         |
| \_hardware MCIERR                 | O dispositivo especificado exibe um problema. Verifique se o dispositivo está funcionando corretamente ou contate o fabricante do dispositivo.                                     |
| MCIERR \_ inválido \_ para \_ \_ abertura automática | O MCI não executará o comando especificado em um dispositivo aberto automaticamente. Aguarde até que o dispositivo seja fechado e tente executar o comando.             |
| MCIERR \_ interno                 | Ocorreu um problema ao inicializar o MCI. Tente reiniciar o sistema operacional Windows.                                                                        |
| \_ID de dispositivo MCIERR inválida \_ \_      | ID de dispositivo inválida. Use a ID fornecida para o dispositivo quando o dispositivo foi aberto.                                                                               |
| MCIERR \_ \_ nome de dispositivo inválido \_    | O dispositivo especificado não está aberto nem reconhecido pelo MCI.                                                                                                     |
| MCIERR \_ \_ arquivo inválido            | O arquivo especificado não pode ser reproduzido no dispositivo MCI especificado. O arquivo pode estar corrompido ou pode usar um formato de arquivo incorreto.                               |
| MCIERR \_ \_ parâmetro ausente       | O comando especificado requer um parâmetro, que você deve fornecer.                                                                                          |
| MCIERR \_ vários                 | Ocorreram erros em mais de um dispositivo. Especifique cada comando e dispositivo separadamente para identificar os dispositivos que estão causando os erros.                             |
| MCIERR \_ deve \_ usar \_ compartilhável     | O driver de dispositivo já está em uso. Você deve especificar o parâmetro "compartilhável" com cada comando Open para compartilhar o dispositivo.                                  |
| MCIERR \_ nenhum \_ elemento \_ permitido     | O dispositivo especificado não usa um nome de arquivo.                                                                                                               |
| MCIERR \_ nenhum \_ inteiro              | O parâmetro para este comando MCI deve ser um valor inteiro.                                                                                                |
| MCIERR \_ sem \_ janela               | Não há janela de exibição.                                                                                                                                 |
| \_função não aplicável \_ MCIERR  | A sequência de comandos MCI especificada não pode ser executada na ordem especificada. Corrigir a sequência de comandos; em seguida, tente novamente.                                   |
| \_bloco de \_ parâmetro \_ nulo MCIERR   | Um bloco de parâmetro nulo (estrutura) foi passado para o MCI.                                                                                                       |
| MCIERR \_ \_ de \_ memória insuficiente          | Seu sistema não tem memória suficiente para esta tarefa. Encerre um ou mais aplicativos para aumentar a memória disponível e tente executar a tarefa novamente. |
| MCIERR \_ OUTOFRANGE               | O valor do parâmetro especificado está fora do intervalo para o comando MCI especificado.                                                                                |
| MCIERR \_ definir \_ CD                  | O arquivo especificado ou o dispositivo MCI está inacessível porque o aplicativo não pode alterar os diretórios.                                                         |
| MCIERR \_ definir \_ unidade               | O arquivo especificado ou o dispositivo MCI está inacessível porque o aplicativo não pode alterar as unidades.                                                              |
| MCIERR \_ recurso sem nome \_        | Não é possível armazenar um arquivo sem nome. Especifique um nome de arquivo.                                                                                                       |
| MCIERR \_ comando não reconhecido \_    | O driver não pode reconhecer o comando especificado.                                                                                                          |
| MCIERR \_ função sem suporte \_    | O driver de dispositivo MCI que o sistema está usando não oferece suporte ao comando especificado.                                                                           |



 

 

 