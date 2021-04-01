---
title: Propriedade IVMMouse ScrollWheelPosition (VPCCOMInterfaces. h)
description: Ajusta a coordenada z do mouse (somente relativo).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Propriedade ScrollWheelPosition Virtual PC
- Propriedade ScrollWheelPosition Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, Propriedade ScrollWheelPosition
topic_type:
- apiref
api_name:
- IVMMouse.ScrollWheelPosition
- IVMMouse.put_ScrollWheelPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e374011dc87ad00d4edef1f33e9787d5a2e6d787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645138"
---
# <a name="ivmmousescrollwheelposition-property"></a>Propriedade IVMMouse:: ScrollWheelPosition

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ajusta a coordenada z do mouse (somente relativo).

Essa propriedade é somente gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScrollWheelPosition(
  [in] long position
);
```



## <a name="property-value"></a>Valor da propriedade

A coordenada z que indica o número de pixels que o mouse deve ser movido ao longo do eixo z.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                     | Significado                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                        | A operação foi bem-sucedida.<br/>                                                                |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>             | A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.<br/>         |
| <dl> <dt>VM \_ E \_ mouse \_ não \_ ativo</dt> <dt>0xA0040800</dt> </dl>           | O dispositivo de mouse não foi ligado ou não está ativo no momento na máquina virtual.<br/> |
| <dl> <dt>VM \_ E \_ usando 0xA0040801 de \_ \_ coordenadas absolutas</dt> <dt></dt> </dl> | A posição da roda de rolagem não pode ser definida quando o dispositivo do mouse está usando coordenadas absolutas.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                  | Ocorreu um erro inesperado.<br/>                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse é definido como ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

