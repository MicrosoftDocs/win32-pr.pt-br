---
title: Extensões de dispositivo para relatar conteúdo adquirido
description: Extensões de dispositivo para relatar conteúdo adquirido
ms.assetid: 597d872e-9105-4edb-afa3-9f4407de0f73
keywords:
- Windows Media Player,extensões de dispositivo
- Windows Media Player, extensões
- Windows Media Player, relatando conteúdo adquirido
- extensões de dispositivo, relatório de conteúdo adquirido
- extensões, relatório de conteúdo adquirido
- relatório de conteúdo adquirido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3389f5b35cedc853d66e6f450836195497628972ea6ae15642d75155d8b83b6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902056"
---
# <a name="device-extensions-for-reporting-acquired-content"></a>Extensões de dispositivo para relatar conteúdo adquirido

Windows Media Player 11 introduz uma nova funcionalidade que permite que dispositivos portáteis notifiquem o Player sobre o conteúdo adicionado ao dispositivo desde a última sincronização. Windows Media Player 11 pode usar essas informações para copiar o conteúdo recém-adquirido do dispositivo para o computador do usuário. Os fabricantes de dispositivos devem observar os seguintes requisitos para dar suporte a essa funcionalidade:

-   Esse recurso só tem suporte para dispositivos habilitados para MTP.
-   Esse recurso funciona apenas com dispositivos que têm uma parceria com Windows Media Player.
-   Os dispositivos devem relatar apenas o conteúdo que o dispositivo foi autor ou baixado. Isso inclui fotos tiradas pelo dispositivo; gravações de voz criadas pelo dispositivo; gravações de 10000001; downloads de um cartão de armazenamento; e downloads da Internet. O conteúdo que foi armazenado no dispositivo como resultado da sincronização com outro dispositivo ou uma parceria diferente não deve ser relatado.

O arquivo de título chamado wmpdevices.h, que é instalado como parte do SDK do Windows Media Player, define as estruturas e constantes necessárias para dar suporte Windows Media Player extensões de dispositivo.

Para que um dispositivo seja reconhecido como suporte ao relatório de conteúdo adquirido por meio do conjunto de extensões de dispositivo Windows Media Player MTP, ele deve incluir as seguintes informações no conjunto de dados DeviceInfo. (Para obter mais informações sobre esse conjuntos de dados, consulte a seção 4.6.1 da especificação de MTP.)



| Campo de conjuntos de dados          | Ordem de campo | Tipo de dados  | Valor                       |
|------------------------|-------------|------------|-----------------------------|
| VendorExtensionID      | 2           | **UINT32** | 0x00000006                  |
| VendorExtensionVersion | 3           | **UINT16** | 0x0064 (100)                |
| VendorExtensionDesc    | 4           | **Cadeia de caracteres** | "microsoft.com/WMPPD: 11.0" |



 

A tabela a seguir fornece detalhes sobre a operação de MTP para relatar conteúdo adquirido.



| Item                  | Descrição                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Código de operação        | 0x9202                                                                                                                                                                                                                          |
| Parâmetro de operação 1 | A ID da transação fornecida pelo dispositivo durante a sessão anterior. Esse valor é zero para a primeira sessão.                                                                                                                |
| Parâmetro de operação 2 | Índice inicial. Esse valor é sempre zero na primeira chamada de uma sessão. Em chamadas subsequentes na mesma sessão de sincronização, esse valor aumenta pela contagem dos itens retornados dos dados de resposta anteriores. |
| Parâmetro de operação 3 | 0x10000. Essa constante, definida em wmpdevices.h, é o número máximo de PUOIDs que podem ser retornados na resposta. Observe que o valor dessa constante pode ser revisado em versões futuras desse arquivo de header.              |
| Parâmetro de operação 4 | 0                                                                                                                                                                                                                               |
| Parâmetro de operação 5 | 0                                                                                                                                                                                                                               |
| Dados                  | O dispositivo retorna uma matriz MTP que contém PUOIDs que foram adquiridos. A matriz começa com um **valor DWORD** que indica a contagem de itens na matriz, seguido pela matriz de elementos .                               |
| Direção dos dados        | R->I                                                                                                                                                                                                                         |
| Opções de código de resposta | **MTP \_ RESPONSE \_ OK** (0x2001) ou código de resposta de erro válido.                                                                                                                                                                    |
| Parâmetro de resposta 1  | A ID da transação atual.                                                                                                                                                                                                     |
| Parâmetro de resposta 2  | O número de PUOIDs que permanecem a ser recuperados por solicitações futuras.                                                                                                                                                            |
| Parâmetro de resposta 3  | **DWORD** que contém informações de status. O status é indicado de maneira bit a bit. Consulte Comentários para obter informações sobre sinalizadores a usar.                                                                                              |
| Parâmetro de resposta 4  | 0                                                                                                                                                                                                                               |
| Parâmetro de resposta 5  | 0                                                                                                                                                                                                                               |



 

## <a name="remarks"></a>Comentários

O status é indicado por meio do Parâmetro de Resposta 3 de maneira bit a bit usando o sinalizador a seguir.



| Sinalizador                                              | Valor | Descrição                                                                                                                                                                                                                             |
|---------------------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SINALIZADORES \_ WMP MDRT \_ ITENS \_ \_ ADQUIRIDOS NÃO \_ REPORTADOS** | 0x1   | O dispositivo contém alguns itens adquiridos que não podem ser retornados na lista de PUOIDS. Observe que esse sinalizador não é redundante com o Parâmetro de Resposta 2. De definir esse sinalizador somente quando houver itens solicitados que o dispositivo não possa retornar. |



 

Os bits 1 a 31 são reservados para uso futuro. Esses bits devem ser definidos como zero.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Windows Media Player**](windows-media-player.md)
</dt> </dl>

 

 




