---
title: DXCoreNotificationType
description: Define constantes que especificam tipos de notificações geradas por objetos [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 3eacd77d2cf15c78a0dc959285874de943fd9130
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084629"
---
# <a name="dxcorenotificationtype-enum"></a>DXCoreNotificationType enum

Define constantes que especificam tipos de notificações geradas por objetos [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) .

Você pode registrar e cancelar o registro para essas notificações chamando [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) e [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), respectivamente.

## <a name="syntax"></a>Syntax

```cpp
enum class DXCoreNotificationType : uint32_t
{
  AdapterListStale = 0,
  AdapterNoLongerValid = 1,
  AdapterBudgetChange = 2,
  AdapterHardwareContentProtectionTeardown = 3
};
```

## <a name="constants"></a>Constantes

### <a name="adapterliststale"></a>AdapterListStale

Essa notificação é gerada por um objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">IDXCoreAdapterList</a> quando a lista de adaptadores se torna obsoleta. A transição atualizada para obsoleta é unidirecional e única, portanto, essa notificação é gerada no máximo uma vez.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Essa notificação é gerada por um objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> quando o adaptador não se torna mais válido. A transição válida para inválida é unidirecional e uma vez, portanto, essa notificação é gerada no máximo uma vez.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Essa notificação é gerada por um objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> quando ocorre uma alteração de orçamento de adaptador. Essa notificação pode ocorrer várias vezes. O uso dessa notificação é funcionalmente semelhante a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3:: RegisterVideoMemoryBudgetChangeNotificationEvent</a>. Em resposta a esse evento, você deve chamar [IDXCoreAdapter:: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (com [DXCoreAdapterState:: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) para avaliar o estado de orçamento da memória atual.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Essa notificação é gerada por um objeto <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">IDXCoreAdapter</a> para notificar a subdivisão de proteção de conteúdo de hardware de um adaptador. Essa notificação pode ocorrer várias vezes. Ele é funcionalmente semelhante a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3:: RegisterHardwareContentProtectionTeardownStatusEvent</a>. Em resposta a esse evento, você deve reavaliar o status da sessão de criptografia atual; por exemplo, chamando [ID3D11VideoContext1:: CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) para determinar o impacto da desmontagem de hardware para uma interface [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) específica.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory:: UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [referência de DXCore](../dxcore-reference.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)