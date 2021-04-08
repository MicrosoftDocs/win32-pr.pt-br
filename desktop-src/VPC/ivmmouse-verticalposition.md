---
title: Propriedade IVMMouse VerticalPosition (VPCCOMInterfaces. h)
description: Coordenada y absoluta do mouse.
ms.assetid: 02fd3677-95d8-44b4-b398-d3ec62e5d9f0
keywords:
- Propriedade VerticalPosition Virtual PC
- Propriedade VerticalPosition Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, Propriedade VerticalPosition
topic_type:
- apiref
api_name:
- IVMMouse.VerticalPosition
- IVMMouse.get_VerticalPosition
- IVMMouse.put_VerticalPosition
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64712f557a3fcd59181e8ce65d835b630da68e48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919099"
---
# <a name="ivmmouseverticalposition-property"></a>Propriedade IVMMouse:: VerticalPosition

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera a coordenada y absoluta do mouse.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_VerticalPosition(
  [in]          long position
);

HRESULT get_VerticalPosition(
  [out, retval] long *position
);
```



## <a name="property-value"></a>Valor da propriedade

A coordenada y que indica a nova posição do mouse. Ao usar coordenadas absolutas, esse valor especifica a nova coordenada y do mouse. Ao usar coordenadas relativas, esse valor especifica o número de pixels que o mouse deve ser movido na direção y.

## <a name="error-codes"></a>Códigos do Erro



| Nome/valor                                                                                                                                                                       | Significado                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ OK</dt> <dt>0</dt> </dl>                                          | A operação foi bem-sucedida.<br/>                                                                                                                |
| <dl> <dt>E \_ </dt> <dt>0X80004003</dt> de ponteiro </dl>                            | O parâmetro é **NULL**.<br/>                                                                                                                   |
| <dl> <dt>VM \_ E a \_ VM \_ não \_ está executando</dt> <dt>0xA0040206</dt> </dl>               | A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.<br/>                                                         |
| <dl> <dt>VM \_ \_Recurso de inclusões E \_ \_ não \_ DISP</dt> . <dt>0xA0040505</dt> </dl> | Os componentes de integração devem ser instalados para recuperar a posição do mouse ou para definir a posição do mouse ao usar coordenadas absolutas.<br/>       |
| <dl> <dt>VM \_ E \_ usando 0xA0040802 de \_ \_ coordenadas relativas</dt> <dt></dt> </dl>   | O dispositivo de mouse está definido atualmente para usar coordenadas relativas do mouse.<br/>                                                                         |
| <dl> <dt>VM \_ E \_ mouse \_ não \_ ativo</dt> <dt>0xA0040800</dt> </dl>             | As coordenadas absolutas não poderão ser recuperadas se o dispositivo de mouse não estiver ligado ou se não estiver ativo no momento na máquina virtual.<br/> |
| <dl> <dt>DISP \_ E \_ </dt> <dt>0x80020009</dt> de exceção </dl>                    | Ocorreu um erro inesperado.<br/>                                                                                                            |



## <a name="remarks"></a>Comentários

Esta propriedade não pode ser recuperada ao usar coordenadas relativas.

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

 

