---
title: Método IVMFloppyDrive AttachHostDrive (VPCCOMInterfaces.h)
description: Anexa uma unidade física no host à unidade de disquete na máquina virtual.
ms.assetid: 9be84e06-e38a-419a-be50-dddd0cc6d2dd
keywords:
- Computador Virtual do método AttachHostDrive
- Computador Virtual do método AttachHostDrive, interface IVMFloppyDrive
- COMPUTADOR Virtual da interface IVMFloppyDrive, método AttachHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8bfdfecc106acd216da5d39e7625f1fbbd9d76190eecc4c2d428595abc9e775
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118595720"
---
# <a name="ivmfloppydriveattachhostdrive-method"></a>Método IVMFloppyDrive::AttachHostDrive

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa uma unidade física no host à unidade de disquete na máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*driveLetter* \[ Em\]
</dt> <dd>

A letra da unidade de disquete física no computador host a ser anexada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                 | Descrição                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                       | A operação foi bem-sucedida.<br/>                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>      | O *parâmetro driveLetter* é **NULL,** não é uma unidade de disquete válida ou o caminho determinado está vazio.<br/> |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl> | A configuração dessa máquina virtual não é válida ou não pode ser encontrada.<br/>                       |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl> | Ocorreu um erro inesperado.<br/>                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte ao cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMFloppyDrive é definido como \_ 661abee6-112a-4ed9-ertf-3c874969f10e<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

