---
title: Extensões de dispositivo MTP para transferência de metadados
description: Extensões de dispositivo MTP para transferência de metadados
ms.assetid: 9cf68373-e84f-4568-a9da-16ddee0fc4e9
keywords:
- Windows Media Player, extensões de dispositivo MTP
- Windows Media Player, extensões de dispositivo
- Windows Media Player,extensões
- Windows Media Player, metadados
- Windows Media Player, protocolo MTP
- Protocolo MTP
- MTP (Protocolo de Transferência de Mídia)
- metadados, extensões de dispositivo MTP
- metadados, extensões de dispositivo
- metadados, extensões
- extensões de dispositivo, transferência de metadados
- extensões, transferência de metadados
- Extensões de dispositivo MTP para transferência de metadados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c56f633d7cd4ca44a90d311c1e4c1c2e6d213e1d2ad1a43b802e4795a59a7d47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572436"
---
# <a name="mtp-device-extensions-for-metadata-transfer"></a>Extensões de dispositivo MTP para transferência de metadados

O Protocolo MTP é um protocolo projetado para dispositivos de mídia portáteis. A principal finalidade desse protocolo é fornecer um protocolo comum para trocar dados entre um computador e um dispositivo de mídia portátil. Isso inclui receber e enviar objetos de mídia e enumerar o conteúdo e os recursos do dispositivo.

O MTP usa PUOIDs (identificadores de objeto exclusivo) persistentes para identificar exclusivamente itens de mídia digital (e outros objetos) armazenados em um dispositivo. Ao trocar informações sobre as alterações ocorridas em um dispositivo que dá suporte a MTP, o dispositivo e Windows Media Player usam PUOIDs para identificar quais objetos foram alterados.

O arquivo de título chamado wmpdevices.h, que é instalado como parte do SDK do Windows Media Player, define as estruturas e constantes necessárias para dar suporte Windows Media Player extensões de dispositivo.

Para que um dispositivo seja reconhecido como suporte à transferência de metadados por meio do conjunto Windows Media Player de extensão de dispositivo MTP, ele deve incluir as seguintes informações no conjunto de dados DeviceInfo. (Para obter mais informações sobre esse conjuntos de dados, consulte a seção 4.6.1 da especificação de MTP.)



| Campo de conjuntos de dados          | Ordem de campo | Tipo de dados  | Valor                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Cadeia de caracteres** | "microsoft.com/WMPPD: 10.0" |



 

A tabela a seguir fornece detalhes sobre a operação MTP para transferência acelerada de metadados.



| Item                  | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operação        | 0x9201                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Parâmetro de operação 1 | A ID da transação fornecida pelo dispositivo durante a sessão anterior. Esse valor é zero para a primeira sessão.                                                                                                                                                                                                                                                                                                                                                                                       |
| Parâmetro de operação 2 | Índice inicial. Esse valor é sempre zero na primeira chamada de uma sessão. Em chamadas subsequentes dentro da mesma sessão de sincronização, esse valor aumenta pela soma da contagem dos itens modificados e excluídos dos dados de resposta anteriores.                                                                                                                                                                                                                                             |
| Parâmetro de operação 3 | 0x10000. Essa constante, definida em wmpdevices.h, é o número máximo de PUOIDs que podem ser retornados na resposta. Observe que o valor dessa constante pode ser revisado em versões futuras desse arquivo de header.                                                                                                                                                                                                                                                                                     |
| Parâmetro de operação 4 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parâmetro de operação 5 | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dados                  | O dispositivo retorna duas matrizes MTP contíguas que contêm PUOIDs. Cada matriz MTP começa com um **valor DWORD** que indica a contagem de itens na matriz, seguido pela matriz de elementos . A primeira matriz MTP contém a lista de PUOIDs que foram adicionados ou alterados. A segunda matriz MTP contém a lista de PUOIDs que foram excluídos do dispositivo portátil. Observe que a soma da contagem de PUOID nas duas matrizes não deve exceder o valor passado no Parâmetro de Operação 3.<br/> |
| Direção dos dados        | R->I                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Opções de código de resposta | **MTP \_ RESPONSE \_ OK** (0x2001) ou código de resposta de erro válido.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Parâmetro de resposta 1  | A ID de transação atual do dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parâmetro de resposta 2  | O número de PUOIDs que permanecem a ser recuperados por solicitações futuras.                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Parâmetro de resposta 3  | **DWORD** que contém informações de status. O status é indicado de maneira bit a bit. Consulte Comentários para obter informações sobre sinalizadores a usar.                                                                                                                                                                                                                                                                                                                                                                     |
| Parâmetro de resposta 4  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Parâmetro de resposta 5  | 0                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

O status é indicado por meio do Parâmetro de Resposta 3 de maneira bit a bit usando os sinalizadores a seguir.



| Sinalizador                                             | Valor | Descrição                                                                                                                                                                                                                          |
|--------------------------------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SINALIZADORES \_ WMP MDRT \_ ITENS \_ \_ EXCLUÍDOS NÃO \_ REPORTADOS** | 0x1   | Os itens foram excluídos antes do primeiro nome do caminho do objeto que está sendo relatado. Isso geralmente indica que o dispositivo foi reformatado.                                                                                                           |
| **SINALIZADORES \_ WMP MDRT \_ ITENS \_ ADICIONADOS NÃO \_ \_ RELATADOS**   | 0x2   | O dispositivo contém alguns itens adicionados que não podem ser retornados na lista de PUOIDS. Observe que esse sinalizador não é redundante com o Parâmetro de Resposta 2. De definir esse sinalizador somente quando houver itens solicitados que o dispositivo não possa retornar. |



 

Os bits 2 a 31 são reservados para uso futuro. Esses bits devem ser definidos como zero.

Windows Media Player envia o comando MTP para um dispositivo no início de uma sessão de sincronização antes que os arquivos de mídia sejam transferidos. O dispositivo deve retornar sua resposta o mais rápido possível para evitar atrasos na operação de sincronização.

Windows Media Player solicitará valores para os atributos listados em [Sobre](about-the-metadata.md) os metadados para cada POUID modificado retornado na resposta. Windows Media Player pode enviar valores atualizados para esses atributos para o dispositivo em comandos subsequentes.

Os arquivos relatados como tendo sido removidos do dispositivo podem ser copiados para o dispositivo novamente se as configurações do usuário exigirem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Extensões de dispositivo para transferência de metadados acelerada**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 





