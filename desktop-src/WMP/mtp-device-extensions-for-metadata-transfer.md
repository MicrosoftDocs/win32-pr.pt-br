---
title: Extensões de dispositivo MTP para transferência de metadados
description: Extensões de dispositivo MTP para transferência de metadados
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Windows Media Player, extensões de dispositivo MTP
- Windows Media Player, extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, metadados
- Windows Media Player, MTP (Media Transfer Protocol)
- MTP (protocolo de transferência de mídia)
- MTP (protocolo de transferência de mídia)
- metadados, extensões de dispositivo MTP
- metadados, extensões de dispositivo
- metadados, extensões
- extensões de dispositivo, transferência de metadados
- extensões, transferência de metadados
- Extensões de dispositivo MTP para transferência de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f64ff16fd97f135d7f8c902af823b967079408fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004842"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>Extensões de dispositivo MTP para transferência de metadados

O MTP (protocolo de transferência de mídia) é um protocolo projetado para dispositivos de mídia portáteis. A principal finalidade desse protocolo é fornecer um protocolo comum para a troca de dados entre um computador e um dispositivo de mídia portátil. Isso inclui o recebimento e o envio de objetos de mídia e a enumeração do conteúdo e dos recursos do dispositivo.

O MTP usa identificadores de objeto exclusivos (PUOIDs) persistentes para identificar exclusivamente os itens de mídia digital (e outros objetos) armazenados em um dispositivo. Ao trocar informações sobre alterações ocorridas em um dispositivo que dá suporte a MTP, o dispositivo e o Windows Media Player usam o PUOIDs para identificar quais objetos foram alterados.

O arquivo de cabeçalho chamado wmpdevices. h, que é instalado como parte do SDK do Windows Media Player, define as estruturas e as constantes necessárias para dar suporte às extensões de dispositivo do Windows Media Player.

Para que um dispositivo seja reconhecido como suporte à transferência de metadados por meio do conjunto de extensão de dispositivo MTP do Windows Media Player, ele deve incluir as seguintes informações no conjunto de dados DeviceInfo. (Para obter mais informações sobre esse conjunto de dados, consulte a seção 4.6.1 da especificação do MTP.)



| Campo de conjunto de          | Ordem dos campos | Tipo de dados  | Valor                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Cadeia de caracteres** | "microsoft.com/WMPPD: 10,0" |



 

A tabela a seguir fornece detalhes sobre a operação de MTP para transferência de metadados acelerada.



| Item                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código da operação        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Parâmetro de operação 1 | A ID da transação fornecida pelo dispositivo durante a sessão anterior. Esse valor é zero para a primeira sessão.                                                                                                                                                                                                                                                                                                                                                                                       |
| Parâmetro de operação 2 | Índice inicial. Esse valor é sempre zero na primeira chamada de uma sessão. Em chamadas subsequentes dentro da mesma sessão de sincronização, esse valor aumenta pela soma da contagem dos itens modificados e excluídos dos dados de resposta anteriores.                                                                                                                                                                                                                                             |
| Parâmetro de operação 3 | 0x10000. Essa constante, definida em wmpdevices. h, é o número máximo de PUOIDs que podem ser retornados na resposta. Observe que o valor dessa constante pode ser revisado em versões futuras desse arquivo de cabeçalho.                                                                                                                                                                                                                                                                                     |
| Parâmetro de operação 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parâmetro de operação 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dados                  | O dispositivo retorna duas matrizes MTP contíguas contendo PUOIDs. Cada matriz de MTP começa com um valor **DWORD** que indica a contagem de itens na matriz, seguida pela matriz de elementos. A primeira matriz de MTP contém a lista de PUOIDs que foram adicionados ou alterados. A segunda matriz de MTP contém a lista de PUOIDs que foram excluídos do dispositivo portátil. Observe que a soma da contagem de PUOID nas duas matrizes não deve exceder o valor passado no parâmetro de operação 3.<br/> |
| Direção dos dados        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Opções de código de resposta | **MTP \_ RESPOSTA \_ OK** (0x2001) ou código de resposta de erro válido.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Parâmetro de resposta 1  | A ID da transação atual do dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parâmetro de resposta 2  | O número de PUOIDs que permanecem para serem recuperadas por solicitações futuras.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parâmetro de resposta 3  | **DWORD** que contém informações de status. O status é indicado de uma maneira bit a bit. Consulte comentários para obter informações sobre sinalizadores a serem usados.                                                                                                                                                                                                                                                                                                                                                                     |
| Parâmetro de resposta 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parâmetro de resposta 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O status é indicado por meio do parâmetro de resposta 3 de maneira unificada usando os sinalizadores a seguir.



| Sinalizador                                             | Valor | Descrição                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_MDRT de \_ \_ \_ itens excluídos não relatados de sinalizadores \_ do WMP** | 0x1   | Os itens foram excluídos antes do nome do primeiro caminho do objeto que está sendo relatado. Isso geralmente indica que o dispositivo foi reformatado.                                                                                                           |
| **o WMP \_ MDRT \_ sinaliza \_ \_ itens adicionados não relatados \_**   | 0x2   | O dispositivo contém alguns itens adicionados que não podem ser retornados na lista de PUOIDS. Observe que esse sinalizador não é redundante com o parâmetro de resposta 2. Defina esse sinalizador somente quando houver itens solicitados que o dispositivo não possa retornar. |



 

Os bits 2 a 31 são reservados para uso futuro. Esses bits devem ser definidos como zero.

O Windows Media Player envia o comando MTP para um dispositivo no início de uma sessão de sincronização antes que os arquivos de mídia sejam transferidos. O dispositivo deve retornar sua resposta o mais rápido possível para evitar atrasos na operação de sincronização.

O Windows Media Player solicitará valores para os atributos listados em [sobre os metadados](about-the-metadata.md) de cada POUID modificado retornado na resposta. O Windows Media Player pode enviar valores atualizados para esses atributos para o dispositivo em comandos subsequentes.

Os arquivos relatados como tendo sido removidos do dispositivo podem ser copiados para o dispositivo novamente se as configurações do usuário exigirem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de dispositivo para transferência de metadados acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





