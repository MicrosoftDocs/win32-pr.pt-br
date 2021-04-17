---
title: Método IVMKeyboard PressAndReleaseKey (VPCCOMInterfaces. h)
description: Simula uma tecla que está sendo pressionada e liberada.
ms.assetid: 2a7fc36f-f1bf-4f1d-b8f7-ea5b167c82a7
keywords:
- PressAndReleaseKey do método virtual PC
- Método PressAndReleaseKey Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método PressAndReleaseKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressAndReleaseKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4adbcac2c79c02ce69584bbfdf21a6b08b350a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105813253"
---
# <a name="ivmkeyboardpressandreleasekey-method"></a>IVMKeyboard: método ressAndReleaseKey de:P

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula uma tecla que está sendo pressionada e liberada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PressAndReleaseKey(
  [in] BSTR key
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

O código de chave da chave a ser pressionada e liberada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                   |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>                                      |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | A cadeia de caracteres especificada está vazia ou contém um código de chave inválido.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                               |



 

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

 

