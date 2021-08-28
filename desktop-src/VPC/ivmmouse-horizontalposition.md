---
title: Propriedade IVMMouse HorizontalPosition (VPCCOMInterfaces.h)
description: Coordenada x absoluta do mouse.
ms.assetid: 8cf2a247-b6db-49f6-8e19-c862004f26cd
keywords:
- Propriedade HorizontalPosition Pc Virtual
- Propriedade HorizontalPosition Pc Virtual , interface IVMMouse
- INTERFACE IVMMouse Pc Virtual, propriedade HorizontalPosition
topic_type:
- apiref
api_name:
- IVMMouse.HorizontalPosition
- IVMMouse.get_HorizontalPosition
- IVMMouse.put_HorizontalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e2cb3fde1caff23845c653024d9c5e2859b0b7b5df8502dbaea167d3e969a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007146"
---
# <a name="ivmmousehorizontalposition-property"></a>Propriedade IVMMouse::HorizontalPosition

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a coordenada X absoluta do mouse.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_HorizontalPosition(
  [in]          long position
);

HRESULT get_HorizontalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valor da propriedade

A coordenada X que indica a nova posição do mouse. Ao usar coordenadas absolutas, esse valor especifica a nova coordenada X do mouse. Ao usar coordenadas relativas, esse valor especifica o número de pixels que o mouse deve ser movido na direção x.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                                                                                |
| <dl> <dt>E \_ PONTEIRO</dt> <dt>0x80004003</dt> </dl>                            | O parâmetro é **NULL.**<br/>                                                                                                                   |
| <dl> <dt>VM \_ E \_ VM \_ NÃO \_ EXECUTANDO</dt> <dt>0XA0040206</dt> </dl>               | A máquina virtual à qual este dispositivo do mouse está anexado não está em execução no momento.<br/>                                                         |
| <dl> <dt>VM \_ O \_ RECURSO DE ADIÇÕES DO E \_ NÃO \_ \_ É</dt> <dt>0XA0040505</dt> </dl> | Os componentes de integração devem ser instalados para recuperar a posição do mouse ou para definir a posição do mouse ao usar coordenadas absolutas.<br/>       |
| <dl> <dt>VM \_ E \_ USANDO \_ \_ COORDENADAS RELATIVAS</dt> <dt>0XA0040802</dt> </dl>   | No momento, o dispositivo mouse está definido para usar coordenadas relativas do mouse.<br/>                                                                         |
| <dl> <dt>VM \_ E \_ MOUSE \_ NÃO \_ ATIVO</dt> <dt>0XA0040800</dt> </dl>             | As coordenadas absolutas não poderão ser recuperadas se o dispositivo do mouse não estiver ligado ou se ele não estiver ativo no momento na máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ EXCEPTION</dt> <dt>0x80020009</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                                                                                                            |



## <a name="remarks"></a>Comentários

Essa propriedade não pode ser recuperada ao usar coordenadas relativas.

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

 

