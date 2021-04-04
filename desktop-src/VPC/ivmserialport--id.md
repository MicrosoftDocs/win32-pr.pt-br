---
title: Método de _ID IVMSerialPort (VPCCOMInterfaces. h)
description: Identificador interno da porta serial.
ms.assetid: c26c18dc-5491-4edf-9338-e4f3bf431084
keywords:
- _ID o método virtual PC
- _ID método virtual PC, interface IVMSerialPort
- IVMSerialPort interface virtual PC, método de _ID
topic_type:
- apiref
api_name:
- IVMSerialPort._ID
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 401e60f301f80f24681ee297d0fb579994561155
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085519"
---
# <a name="ivmserialport_id-method"></a>Método IVMSerialPort:: \_ ID

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera o identificador interno da porta serial.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT _ID(
  [out] long *portID
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*portaid* \[ fora\]
</dt> <dd>

O identificador da porta serial.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                 | Descrição                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                            |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>         | O parâmetro é **NULL**.<br/>                               |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl> | Ocorreu um erro inesperado.<br/>                        |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl> | A configuração desta máquina virtual não é válida.<br/> |



 

## <a name="remarks"></a>Comentários

Essa propriedade não pode ser usada por linguagens de script.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMSerialPort é definido como 2ce4460d-1d3f-4458-bf8b-44084b816815<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMSerialPort**](ivmserialport.md)
</dt> </dl>

 

