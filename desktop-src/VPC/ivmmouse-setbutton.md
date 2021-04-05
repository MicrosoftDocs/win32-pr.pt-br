---
title: Método SetButton IVMMouse (VPCCOMInterfaces. h)
description: Define o estado atual (para cima ou para baixo) do botão do mouse especificado.
ms.assetid: 52b24472-68d6-4a42-8ae5-b1434a6d67f3
keywords:
- Método SetButton Virtual PC
- Método SetButton Virtual PC, interface IVMMouse
- IVMMouse interface virtual PC, método SetButton
topic_type:
- apiref
api_name:
- IVMMouse.SetButton
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2d30ae131ac33eeff339b98511fd2da60a1e606
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086221"
---
# <a name="ivmmousesetbutton-method"></a>Método IVMMouse:: SetButton

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Define o estado atual (para cima ou para baixo) do botão do mouse especificado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetButton(
  [in] VMMouseButton buttonIndex,
  [in] VARIANT_BOOL  down
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*buttonIndex* \[ no\]
</dt> <dd>

O índice do botão. Para obter uma lista de valores, consulte [**VMMouseButton**](vmmousebutton.md).

</dd> <dt>

*para baixo* \[ no\]
</dt> <dd>

O novo estado do botão. Use **true** se o estado do botão for para ser definido como Down e **false** se for definido como up.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                        | Descrição                                                                                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                              | A operação foi bem-sucedida.<br/>                                                                                                          |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>             | O parâmetro *buttonIndex* não é válido.<br/>                                                                                              |
| <dl> <dt>**VM \_ E a \_ VM \_ não \_ está executando**</dt> <dt>0xA0040206</dt> </dl>   | A máquina virtual à qual este dispositivo de mouse está anexado não está em execução no momento.<br/>                                                   |
| <dl> <dt>**VM \_ E \_ mouse \_ não \_ ativo**</dt> <dt>0xA0040800</dt> </dl> | A operação não pôde ser concluída porque o dispositivo de mouse não está ligado ou não está ativo no momento na máquina virtual.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>        | Ocorreu um erro inesperado.<br/>                                                                                                      |



 

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

 

