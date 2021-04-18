---
description: A interface ITFormatControl expõe métodos que permitem que um aplicativo recupere informações relacionadas ao formato de um fluxo de recebimento ou de transmissão para uma chamada.
ms.assetid: a3d15561-229e-4eb6-a0ac-2d69f170bced
title: Interface ITFormatControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0735e7bfaf5222948cef5e047530a35cb19a125
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767755"
---
# <a name="itformatcontrol-interface"></a>Interface ITFormatControl

\[ Essa interface não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITFormatControl** expõe métodos que permitem que um aplicativo recupere informações relacionadas ao formato de um fluxo de recebimento ou de transmissão para uma chamada.

Essa interface é implementada pelo seu [H323 MSP](h323-msp.md) e é exposta somente quando uma chamada usa esse provedor de serviços.

## <a name="members"></a>Membros

A interface **ITFormatControl** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITFormatControl** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITFormatControl** tem esses métodos.



| Método                                                                     | Descrição                                                                    |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetCurrentFormat**](itformatcontrol-getcurrentformat.md)               | Obtém o formato de mídia do fluxo atual.<br/>                        |
| [**GetNumberOfCapabilities**](itformatcontrol-getnumberofcapabilities.md) | Obtém o número de recursos associados ao formato atual.<br/> |
| [**GetStreamCaps**](itformatcontrol-getstreamcaps.md)                     | Obtém os recursos associados a um determinado índice de formato.<br/>         |
| [**ReleaseFormat**](itformatcontrol-releaseformat.md)                     | Libera a estrutura associada ao formato.<br/>                  |
| [**ReOrderCapabilities**](itformatcontrol-reordercapabilities.md)         | Define um novo pedido para recursos de formato.<br/>                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



 

