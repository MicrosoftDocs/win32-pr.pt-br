---
title: Método de _ID IVMParallelPort (VPCCOMInterfaces.h)
description: Recupera o identificador interno da porta paralela.
ms.assetid: a0de74da-0e23-489e-8a89-8deba974e548
keywords:
- _ID computador virtual do método
- _ID método Virtual PC, interface IVMParallelPort
- Interface IVMParallelPort para o método _ID virtual
topic_type:
- apiref
api_name:
- IVMParallelPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0c7b3eab7de47d182c94aa9b5fb35aef04e98495ef3e7b39d4547967f3438b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118593214"
---
# <a name="ivmparallelport_id-method"></a>MÉTODO IVMParallelPort:: \_ ID

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o identificador interno da porta paralela.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*portID* \[ out\]
</dt> <dd>

O identificador de porta paralela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                 | Descrição                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                            |
| <dl> <dt>**E \_ PONTEIRO**</dt> <dt>0x80004003</dt> </dl>         | O parâmetro é **NULL.**<br/>                               |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/>                        |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | A configuração dessa máquina virtual não é válida.<br/> |



 

## <a name="remarks"></a>Comentários

Essa propriedade não é acessível por linguagens de script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMParallelPort é definido como \_ 097beecb-0a02-474f-field6-298b22293fc6<br/>            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMParallelPort**](ivmparallelport.md)
</dt> </dl>

 

