---
title: Propriedade IVMMouse ScrollWheelPosition (VPCCOMInterfaces.h)
description: Ajusta a coordenada z do mouse (somente relativo).
ms.assetid: 52269d0c-a7a8-4dc2-bb27-c891d1e9c293
keywords:
- Propriedade ScrollWheelPosition Pc Virtual
- Propriedade ScrollWheelPosition pc virtual, interface IVMMouse
- INTERFACE IVMMouse Pc Virtual, propriedade ScrollWheelPosition
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
ms.openlocfilehash: 334190707cd43e63ce2244f410180b11bf6eb5018ff1482f073903adfb4b7878
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510646"
---
# <a name="ivmmousescrollwheelposition-property"></a>Propriedade IVMMouse::ScrollWheelPosition

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

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
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0XA0040206</dt> </dl>             | A máquina virtual à qual este dispositivo do mouse está anexado não está em execução no momento.<br/>         |
| <dl> <dt>VM \_ E \_ MOUSE \_ NÃO \_ ATIVO</dt> <dt>0XA0040800</dt> </dl>           | O dispositivo do mouse não foi ligado ou não está ativo na máquina virtual no momento.<br/> |
| <dl> <dt>VM \_ E \_ USANDO \_ \_ COORDENADAS ABSOLUTAS</dt> <dt>0XA0040801</dt> </dl> | A posição da roda de rolagem não pode ser definida quando o dispositivo do mouse está usando coordenadas absolutas.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                  | Ocorreu um erro inesperado.<br/>                                                            |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMmouse é definido como \_ ac903f6d-6346-4f29-8875-5d511a13895e<br/>                   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

