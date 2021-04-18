---
title: Extensões de dispositivo para relatórios de conteúdo adquirido
description: Extensões de dispositivo para relatórios de conteúdo adquirido
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Windows Media Player, extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, relatando conteúdo adquirido
- extensões de dispositivo, relatórios de conteúdo adquirido
- extensões, relatando conteúdo adquirido
- relatando conteúdo adquirido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 831312457427cc9fe4ceed004772f3b174f77989
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758224"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Extensões de dispositivo para relatórios de conteúdo adquirido

O Windows Media Player 11 apresenta uma nova funcionalidade que permite que os dispositivos portáteis notifiquem o Player sobre o conteúdo adicionado ao dispositivo desde a última sincronização. O Windows Media Player 11 pode usar essas informações para copiar o conteúdo adquirido recentemente do dispositivo para o computador do usuário. Os fabricantes de dispositivos devem observar os seguintes requisitos para dar suporte a essa funcionalidade:

-   Esse recurso tem suporte apenas para dispositivos habilitados para MTP.
-   Esse recurso funciona apenas com dispositivos que têm uma parceria com o Windows Media Player.
-   Os dispositivos devem relatar apenas o conteúdo que o dispositivo criou ou baixou. Isso inclui fotos tiradas pelo dispositivo; gravações de voz criadas pelo dispositivo; gravações de caixa postal; downloads de um cartão de memória; e downloads da Internet. O conteúdo que foi armazenado no dispositivo como resultado da sincronização com outro dispositivo ou uma parceria diferente não deve ser relatado.

O arquivo de cabeçalho chamado wmpdevices. h, que é instalado como parte do SDK do Windows Media Player, define as estruturas e as constantes necessárias para dar suporte às extensões de dispositivo do Windows Media Player.

Para que um dispositivo seja reconhecido como compatível com o relatório de conteúdo adquirido por meio do conjunto de extensão de dispositivo MTP do Windows Media Player, ele deve incluir as seguintes informações no conjunto de dados DeviceInfo. (Para obter mais informações sobre esse conjunto de dados, consulte a seção 4.6.1 da especificação do MTP.)



| Campo de conjunto de          | Ordem dos campos | Tipo de dados  | Valor                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Cadeia de caracteres** | "microsoft.com/WMPPD: 11,0" |



 

A tabela a seguir fornece detalhes sobre a operação de MTP para relatar conteúdo adquirido.



| Item                  | Descrição                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código da operação        | 0x9202                                                                                                                                                                                                                          |
| Parâmetro de operação 1 | A ID da transação fornecida pelo dispositivo durante a sessão anterior. Esse valor é zero para a primeira sessão.                                                                                                                |
| Parâmetro de operação 2 | Índice inicial. Esse valor é sempre zero na primeira chamada de uma sessão. Em chamadas subsequentes dentro da mesma sessão de sincronização, esse valor aumenta pela contagem dos itens retornados dos dados de resposta anteriores. |
| Parâmetro de operação 3 | 0x10000. Essa constante, definida em wmpdevices. h, é o número máximo de PUOIDs que podem ser retornados na resposta. Observe que o valor dessa constante pode ser revisado em versões futuras desse arquivo de cabeçalho.              |
| Parâmetro de operação 4 | 0                                                                                                                                                                                                                               |
| Parâmetro de operação 5 | 0                                                                                                                                                                                                                               |
| Dados                  | O dispositivo retorna uma matriz de MTP que contém PUOIDs que foram adquiridos. A matriz começa com um valor **DWORD** que indica a contagem de itens na matriz, seguida pela matriz de elementos.                               |
| Direção dos dados        | R->I                                                                                                                                                                                                                         |
| Opções de código de resposta | **MTP \_ RESPOSTA \_ OK** (0x2001) ou código de resposta de erro válido.                                                                                                                                                                    |
| Parâmetro de resposta 1  | A ID da transação atual.                                                                                                                                                                                                     |
| Parâmetro de resposta 2  | O número de PUOIDs que permanecem para serem recuperadas por solicitações futuras.                                                                                                                                                            |
| Parâmetro de resposta 3  | **DWORD** que contém informações de status. O status é indicado de uma maneira bit a bit. Consulte comentários para obter informações sobre sinalizadores a serem usados.                                                                                              |
| Parâmetro de resposta 4  | 0                                                                                                                                                                                                                               |
| Parâmetro de resposta 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

O status é indicado por meio do parâmetro de resposta 3 de maneira unificada usando o sinalizador a seguir.



| Sinalizador                                              | Valor | Descrição                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MDRT do WMP \_ \_ sinalizadores de \_ \_ itens ADQUIRIdos não relatados \_** | 0x1   | O dispositivo contém alguns itens adquiridos que não podem ser retornados na lista de PUOIDS. Observe que esse sinalizador não é redundante com o parâmetro de resposta 2. Defina esse sinalizador somente quando houver itens solicitados que o dispositivo não possa retornar. |



 

Os bits de 1 a 31 são reservados para uso futuro. Esses bits devem ser definidos como zero.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




