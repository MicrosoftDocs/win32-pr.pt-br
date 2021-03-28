---
description: Mensagens de erro da função de pacote de fontes
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Mensagens de erro da função de pacote de fontes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bcf84f92b60351e8375df682de0c3b01c2aa1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091181"
---
# <a name="font-package-function-error-messages"></a>Mensagens de erro da função de pacote de fontes

Os valores longos a seguir são retornados pelas funções de pacote de fonte ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) e [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ) quando são encontrados erros. Quando as funções forem bem-sucedidas, o valor nenhum \_ erro será retornado.



| Retornar valor                   | Valor | Descrição                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| SEM \_ erros                      | 0     | Não ocorreu nenhum erro.                                                                                               |
| formato de erro \_                    | 1006  | Ocorreu um erro de formato de dados de entrada.                                                                             |
| ERR \_ Generic                   | 1000  | Ocorreu um erro no código genérico.                                                                               |
| ERRO \_ mem                       | 1005  | Ocorreu um erro durante a alocação de memória.                                                                      |
| \_não erro sem \_ glifos                | 1009  | Nenhum glifo foi encontrado.                                                                                            |
| \_base inválida de Err \_             | 1085  | A fonte continha uma tabela de dados de linha de base inválida (BASE). Atualmente, esse valor não é usado.                      |
| ERRO \_ de \_ CMap inválido             | 1030  | A fonte continha uma tabela de mapeamento de caractere para glifos (CMap) inválida.                                           |
| ERRO \_ de \_ formato Delta inválido \_    | 1013  | Um formato Delta inválido foi detectado durante a tentativa de subconjunto de uma fonte de formato 1 ou 2.                                |
| ERRO \_ \_ EBLC inválido             | 1086  | A fonte continha uma tabela de dados de local de bitmap inserida (EBLC) inválida.                                        |
| ERRO \_ \_ GLYF inválido             | 1061  | A fonte continha uma tabela de dados de glifo (glyf) inválida.                                                           |
| ERRO \_ \_ GDEF inválido             | 1083  | A fonte continha uma tabela inválida de dados de definição de glifos (GDEF). Atualmente, esse valor não é usado.              |
| ERRO de \_ GPOs inválidos \_             | 1082  | A fonte continha uma tabela de dados de posicionamento de glifos (GPOS) inválida. Atualmente, esse valor não é usado.             |
| ERRO \_ \_ GSUB inválido             | 1081  | A fonte continha uma tabela inválida de dados de substituição de glifo (GSUB).                                              |
| ERRO \_ \_ HDMX inválido             | 1089  | A fonte continha uma tabela de métricas de dispositivo horizontal (hdmx) inválida.                                            |
| \_cabeça inválida de Err \_             | 1062  | A fonte continha uma tabela inválida de cabeçalho de fonte (cabeçalho).                                                          |
| ERRO \_ \_ HHEA inválido             | 1063  | A fonte continha uma tabela de cabeçalho horizontal inválida (hhea).                                                    |
| ERR \_ \_ HHEA \_ ou \_ VHEA inválido   | 1072  | A fonte continha uma tabela inválida de cabeçalho horizontal (hhea) ou uma tabela vhea (cabeçalho de métrica vertical) inválida. |
| ERRO \_ \_ HMTX inválido             | 1064  | A fonte continha uma tabela de métricas horizontais (hmtx) inválida.                                                   |
| ERR \_ \_ HMTX \_ ou \_ VMTX inválido   | 1073  | A fonte continha uma tabela de métricas horizontais (hmtx) inválida ou uma tabela de vmtx (métrica vertical inválida).       |
| ERRO \_ \_ JSTF inválido             | 1084  | A fonte continha uma tabela de dados de justificativa (JSTF) inválida.                                                   |
| ERRO \_ \_ ltsh inválido             | 1087  | A fonte continha uma tabela inválida de dados de limite linear (LTSH).                                                |
| ERRO \_ \_ para inválido              | 1080  | A fonte era uma fonte TrueType aberta inválida.                                                                      |
| ERRO \_ \_ VDMX inválido             | 1088  | A fonte continha uma tabela de métricas de dispositivo vertical (VDMX) inválida.                                              |
| ERRO \_ de \_ localizável inválido             | 1065  | A fonte continha um índice inválido para a tabela local (locais).                                                    |
| ERRO \_ \_ MAXP inválido             | 1066  | A fonte continha uma tabela de perfil máximo (maxp) inválida.                                                      |
| ERRO \_ ao \_ mesclar somas de verificação inválidas \_ | 1011  | Uma tentativa de Mesclar somas de verificação para duas fontes de uma fonte de mãe diferente não foi bem-sucedida.                       |
| ERRO \_ de \_ formatos de mesclagem inválidos \_   | 1010  | Uma tentativa de Mesclar fontes com os formatos de dttf incorretos não foi bem-sucedida.                                          |
| ERRO \_ de \_ mesclagem inválido \_ NUMGLYPHS | 1012  | Uma tentativa de mesclar o número de glifos para duas fontes de uma fonte de mãe diferente não foi bem-sucedida.            |
| \_nome inválido de erro \_             | 1067  | O nome do pacote de fontes ou um nome de fonte era inválido.                                                                |
| ERRO \_ \_ post inválido             | 1068  | A fonte continha uma tabela inválida de informações PostScript (post).                                               |
| ERRO \_ \_ OS2 inválido              | 1069  | A fonte continha uma tabela inválida de SO/2 e métricas específicas do Windows (SO/2).                                    |
| ERRO \_ \_ VHEA inválido             | 1070  | A fonte continha uma tabela inválida de cabeçalho de métrica vertical (vhea).                                              |
| ERRO \_ \_ VMTX inválido             | 1071  | A fonte continha uma tabela vmtx (métrica vertical) inválida.                                                     |
| ERRO \_ de \_ índice TTC inválido \_       | 1015  | Um índice inválido de base zero (TTC) no arquivo de fonte foi passado.                                                 |
| ERRO \_ de \_ CMap ausente             | 1030  | A fonte não continha uma tabela de CMap.                                                                           |
| ERRO \_ \_ EBDT ausente             | 1044  | A fonte não continha uma tabela EBDT.                                                                          |
| ERRO \_ \_ GLYF ausente             | 1031  | A fonte não continha uma tabela glyf.                                                                           |
| \_falta a \_ cabeça do erro             | 1032  | A fonte não continha uma tabela de cabeçalho.                                                                           |
| ERRO \_ \_ HHEA ausente             | 1046  | A fonte não continha uma tabela hhea.                                                                          |
| ERRO \_ \_ HMTX ausente             | 1034  | A fonte não continha uma tabela hmtx.                                                                          |
| ERRO \_ \_ localizável ausente             | 1035  | A fonte não continha uma tabela localizável.                                                                           |
| ERRO \_ \_ MAXP ausente             | 1036  | A fonte não continha uma tabela maxp.                                                                           |
| ERRO \_ \_ nome ausente             | 1037  | A fonte não continha uma tabela de nomenclatura (nome).                                                                  |
| ERRO \_ na \_ postagem ausente             | 1038  | A fonte não continha uma tabela post.                                                                           |
| ERRO \_ \_ OS2 ausente              | 1039  | A fonte não continha uma tabela do sistema operacional/2.                                                                          |
| ERRO \_ \_ VHEA ausente             | 1040  | A fonte não continha uma tabela vhea.                                                                           |
| ERRO \_ \_ VMTX ausente             | 1041  | A fonte não continha uma tabela vmtx.                                                                           |
| ERR \_ ausente \_ HHEA \_ ou \_ VHEA   | 1042  | A fonte não continha uma tabela hhea ou uma tabela vhea.                                                          |
| ERR \_ ausente \_ HMTX \_ ou \_ VMTX   | 1043  | A fonte não continha uma tabela hmtx ou uma tabela vmtx.                                                          |
| ERRO \_ não \_ TTC                  | 1014  | O valor fornecido não era um índice para um arquivo TTC.                                                              |
| PARAMETER0 de erro \_                | 1100  | O parâmetro de função de chamada 0 era inválido.                                                                        |
| ERRO \_ parâmetro1                | 1101  | A chamada do parâmetro de função 1 era inválida.                                                                        |
| ERRO \_ parâmetro2                | 1102  | O parâmetro de função de chamada 2 era inválido.                                                                        |
| ERRO \_ parâmetro3                | 1103  | O parâmetro de função de chamada 3 era inválido.                                                                        |
| ERRO \_ parâmetro4                | 1104  | O parâmetro de função de chamada 4 era inválido.                                                                        |
| PARAMETER5 de erro \_                | 1105  | O parâmetro de função de chamada 5 era inválido.                                                                        |
| PARAMETER6 de erro \_                | 1106  | O parâmetro de função de chamada 6 era inválido.                                                                        |
| PARAMETER7 de erro \_                | 1107  | A chamada do parâmetro de função 7 era inválida.                                                                        |
| PARAMETER8 de erro \_                | MaxPrintersPerSession을 마우스 오른쪽 단추로 클릭한 다음 수정을 클릭합니다.  | O parâmetro de função de chamada 8 era inválido.                                                                        |
| PARAMETER9 de erro \_                | 1109  | O parâmetro de função de chamada 9 era inválido.                                                                        |
| PARAMETER10 de erro \_               | 1110  | O parâmetro de função de chamada 10 era inválido.                                                                       |
| PARAMETER11 de erro \_               | 1111  | O parâmetro de função de chamada 11 era inválido.                                                                       |
| PARAMETER12 de erro \_               | 1112  | O parâmetro de função de chamada 12 era inválido.                                                                       |
| PARAMETER13 de erro \_               | Etapas de resolução para o seguinte evento ID 1113  | O parâmetro de função de chamada 13 era inválido.                                                                       |
| PARAMETER14 de erro \_               | 1114  | A chamada do parâmetro de função 14 era inválida.                                                                       |
| PARAMETER15 de erro \_               | 1115  | O parâmetro de função de chamada 15 era inválido.                                                                       |
| PARAMETER16 de erro \_               | 1116  | A chamada do parâmetro de função 16 era inválida.                                                                       |
| READCONTROL de erro \_               | 1003  | A estrutura de controle de leitura não correspondeu aos dados.                                                                   |
| READOUTOFBOUNDS de erro \_           | 1001  | Uma leitura da memória não foi permitida, possivelmente porque os dados estavam fora dos limites ou estão corrompidos.                          |
| versão de erro \_                   | 1008  | O valor de dttf. Version principal dos dados de entrada era maior que a versão que a função pode ler.                   |
| o \_ erro \_ aumentaria               | 1007  | A ação solicitada fez com que os dados aumentassem e o aplicativo deve usar dados originais.                             |
| WRITECONTROL de erro \_              | 1004  | A estrutura de controle de gravação não correspondeu aos dados.                                                                  |
| WRITEOUTOFBOUNDS de erro \_          | 1002  | Uma gravação na memória não foi permitida, possivelmente porque os dados estavam fora dos limites.                                      |



 

 

 



