---
title: Método IVMKeyboard TypeAsciiText (VPCCOMInterfaces. h)
description: Simula uma série de chaves ASCII que estão sendo digitadas no convidado.
ms.assetid: 6c7fbfed-d495-4f11-a7d1-dc08bd075870
keywords:
- TypeAsciiText do método virtual PC
- Método TypeAsciiText Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método TypeAsciiText
topic_type:
- apiref
api_name:
- IVMKeyboard.TypeAsciiText
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 538df9fc3036e43dc36f4ca7425688157e9fca77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085753"
---
# <a name="ivmkeyboardtypeasciitext-method"></a>Método IVMKeyboard:: TypeAsciiText

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula uma série de chaves ASCII que estão sendo digitadas no convidado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT TypeAsciiText(
  [in] BSTR text
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*texto* \[ de no\]
</dt> <dd>

A cadeia de caracteres de texto ASCII a ser digitada na máquina virtual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>     |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | A cadeia de caracteres especificada está vazia.<br/>    |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

