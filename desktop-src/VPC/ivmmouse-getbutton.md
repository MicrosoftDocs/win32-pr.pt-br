---
title: Método IVMMouse GetButton (VPCCOMInterfaces.h)
description: Recupera o estado atual do botão do mouse especificado.
ms.assetid: eb534f88-387d-42fb-bfc3-bca17685021e
keywords:
- Computador Virtual do método GetButton
- Método GetButton Pc Virtual, interface IVMMouse
- INTERFACE IVMMouse Virtual PC , método GetButton
topic_type:
- apiref
api_name:
- IVMMouse.GetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af37a303c90fb9c60020f19f22767ec508c53fdc54bcefa533dabc780c38f16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007156"
---
# <a name="ivmmousegetbutton-method"></a>Método IVMMouse::GetButton

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o estado atual (para cima ou para baixo) do botão do mouse especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetButton(
  [in]          VMMouseButton buttonIndex,
  [out, retval] VARIANT_BOOL  *isDown
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*buttonIndex* \[ Em\]
</dt> <dd>

O índice do botão cujo estado está sendo solicitado. Para ver uma lista de valores, [**consulte VMMouseButton**](vmmousebutton.md).

</dd> <dt>

*isDown* \[ out, retval\]
</dt> <dd>

O estado do botão indicado. **TRUE** se o botão estiver na máquina virtual no momento; caso contrário, **FALSE.**

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                        | Descrição                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | A operação foi bem-sucedida.<br/>                                                        |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>                | O *parâmetro isDown* é **NULL.**<br/>                                                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | O *parâmetro buttonIndex* não é válido.<br/>                                            |
| <dl> <dt>**VM \_ E \_ VM \_ NÃO \_ EXECUTANDO**</dt> <dt>0XA0040206</dt> </dl>   | A máquina virtual à qual este dispositivo do mouse está anexado não está em execução no momento.<br/> |
| <dl> <dt>**VM \_ E \_ MOUSE NÃO ATIVO \_ \_ 0XA0040800**</dt> <dt></dt> </dl> | O dispositivo do mouse não foi ligado.<br/>                                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>        | Ocorreu um erro inesperado.<br/>                                                    |



 

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

 

