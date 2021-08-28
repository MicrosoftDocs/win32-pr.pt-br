---
title: DXCoreNotificationType
description: Define constantes que especificam tipos de notificações gerados por [objetos IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 230b6c103f83e72dfe0ba7803cde4b4695a32de724ce44c1aaccf5131d077bad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726006"
---
# <a name="dxcorenotificationtype-enum"></a>Enum DXCoreNotificationType

Define constantes que especificam tipos de notificações gerados por [objetos IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList.](./nn-dxcore_interface-idxcoreadapterlist.md)

Você pode registrar e não registrar essas notificações chamando [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) e [IDXCoreAdapterFactory::UnregisterEventNotification,](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md)respectivamente.

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

Essa notificação é aplicável por <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapterlist">um objeto IDXCoreAdapterList</a> quando a lista de adaptadores fica desalocada. A transição nova para desalocada é única e única, portanto, essa notificação é aplicável no máximo uma vez.

### <a name="adapternolongervalid"></a>AdapterNoLongerValid

Essa notificação é aedida por <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">um objeto IDXCoreAdapter</a> quando o adaptador deixa de ser válido. A transição válida para inválida é única e única, portanto, essa notificação é a mais uma vez.

### <a name="adapterbudgetchange"></a>AdapterBudgetChange

Essa notificação é aumentada por <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">um objeto IDXCoreAdapter</a> quando ocorre uma alteração no orçamento do adaptador. Essa notificação pode ocorrer muitas vezes. O uso dessa notificação é funcionalmente semelhante ao <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent">IDXGIAdapter3::RegisterVideoMemoryBudgetChangeNotificationEvent.</a> Em resposta a esse evento, você deve chamar [IDXCoreAdapter::QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) (com [DXCoreAdapterState::AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md)) para avaliar o estado atual do orçamento de memória.

### <a name="adapterhardwarecontentprotectionteardown"></a>AdapterHardwareContentProtectionTeardown

Essa notificação é aedida por <a href="/windows/win32/dxcore/dxcore_interface/nn-dxcore_interface-idxcoreadapter">um objeto IDXCoreAdapter</a> para notificar sobre a rebaixamento da proteção de conteúdo de hardware de um adaptador. Essa notificação pode ocorrer muitas vezes. Ele é funcionalmente semelhante a <a href="/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registerhardwarecontentprotectionteardownstatusevent">IDXGIAdapter3::RegisterHardwareContentProtectionTeardownStatusEvent</a>. Em resposta a esse evento, você deve reavalidar o status da sessão de criptografia atual; por exemplo, chamando [ID3D11VideoContext1::CheckCryptoSessionStatus](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-checkcryptosessionstatus) para determinar o impacto da redução de hardware para uma interface [ID3D11CryptoSession](/windows/win32/api/d3d11/nn-d3d11-id3d11cryptosession) específica.

## <a name="see-also"></a>Confira também

[IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), [IDXCoreAdapterFactory::UnregisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md), [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [Referência de DXCore](../dxcore-reference.md), Usando [DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)