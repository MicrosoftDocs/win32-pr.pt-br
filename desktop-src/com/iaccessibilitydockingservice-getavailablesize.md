---
title: Método IAccessibilityDockingService GetAvailableSize
description: Obtém as dimensões disponíveis para o encaixe de uma janela de acessibilidade em um monitor.
ms.assetid: 1C838B01-EF26-4FCC-878F-A36DEFBA3142
keywords:
- Método COM de GetAvailableSize
- Método GetAvailableSize COM, interface IAccessibilityDockingService
- IAccessibilityDockingService interface COM, método GetAvailableSize
topic_type:
- apiref
api_name:
- IAccessibilityDockingService.GetAvailableSize
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e1b9f113792b14f5fb86e0349d083ea48ffdb3fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006486"
---
# <a name="iaccessibilitydockingservicegetavailablesize-method"></a>Método IAccessibilityDockingService:: GetAvailableSize

Obtém as dimensões disponíveis para o encaixe de uma janela de acessibilidade em um monitor.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAvailableSize(
  [in]  HMONITOR hMonitor,
  [out] UINT     *puMaxHeight,
  [out] UINT     *puFixedWidth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HMONITOR* \[ no\]
</dt> <dd>

Especifica o monitor para o qual o tamanho de encaixe disponível será recuperado.

</dd> <dt>

*puMaxHeight* \[ fora\]
</dt> <dd>

Em caso de sucesso, defina para a altura máxima disponível para encaixe no *HMONITOR* especificado, em pixels.

Em caso de falha, defina como zero.

</dd> <dt>

*puFixedWidth* \[ fora\]
</dt> <dd>

Em caso de sucesso, defina a largura fixa disponível para encaixe no *HMONITOR* especificado, em pixels. Qualquer janela encaixada neste *HMONITOR* será dimensionada para essa largura.

Em caso de falha, defina como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor



| Código de retorno                                                                                                                          | Descrição                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                                                 | Êxito.<br/>                                                              |
| <dl> <dt>**HRESULT \_ do \_ Win32 (erro \_ \_ identificador de monitor inválido \_ )**</dt> </dl> | O monitor especificado pelo identificador de monitor não oferece suporte ao encaixe.<br/> |



 

Se *puMaxHeight* ou *puFixedWidth* forem nulos, ocorrerá uma violação de acesso.

## <a name="remarks"></a>Comentários

As janelas de acessibilidade só podem ser encaixadas em um monitor que tenha pelo menos 768 pixels de tela vertical. Essa API não permitirá que essas janelas sejam encaixadas com uma altura que faria com que os aplicativos da Windows Store tenham menos de 768 pixels de tela vertical.

## <a name="examples"></a>Exemplos


```
IAccessibilityDockingService *pDockingService;
HRESULT hr = CoCreateInstance(CLSID_AccessibilityDockingService, CLSCTX_INPROV_SERVER, nullptr, IID_PPV_ARGS(&pDockingService));
if (SUCCEEDED(hr))
{
    UINT uMaxHeight;
    UINT uFixedWidth;

    HMONITOR hMonitor = MonitorFromWindow(_hwndMyApplication, MONITOR_DEFAULTTONULL);
    if (hMonitor != nullptr)
    {
        hr = pDockingService->GetAvailableSize(hMonitor, &uMaxHeight, &uFixedWidth);
    }
}
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IAccessibilityDockingService**](/windows/desktop/api/shobjidl/nn-shobjidl-iaccessibilitydockingservice)
</dt> </dl>

 

 





