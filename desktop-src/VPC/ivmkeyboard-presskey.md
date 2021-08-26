---
title: Método IVMKeyboard PressKey (VPCCOMInterfaces. h)
description: Simula uma tecla que está sendo pressionada.
ms.assetid: d945128a-ffde-465c-b615-83a1d5dc789f
keywords:
- PressKey do método virtual PC
- Método PressKey Virtual PC, interface IVMKeyboard
- IVMKeyboard interface virtual PC, método PressKey
topic_type:
- apiref
api_name:
- IVMKeyboard.PressKey
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e84e72e28743cea893d5b0518e138fdda51af4b49f30eb8b516a6ae2f984f08
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959066"
---
# <a name="ivmkeyboardpresskey-method"></a>IVMKeyboard: método ressKey de:P

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Simula uma tecla que está sendo pressionada.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT PressKey(
  [in] BSTR key
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ no\]
</dt> <dd>

O código de chave para a chave a ser pressionada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMKeyboard é definido como 00695f2e-c5ad-4d6e-B1ab-336ed121f8c4<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMKeyboard**](ivmkeyboard.md)
</dt> </dl>

 

