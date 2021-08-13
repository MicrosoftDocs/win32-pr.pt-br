---
title: Método IVMFloppyDrive ReleaseHostDrive (VPCCOMInterfaces.h)
description: Libera uma unidade física no host da unidade de disquete.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- Pc Virtual do método ReleaseHostDrive
- Método ReleaseHostDrive Pc Virtual, interface IVMFloppyDrive
- COMPUTADOR Virtual da interface IVMFloppyDrive, método ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMFloppyDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b44202754528483f88ab045b848e83a6a41a318b1e1ffed6122c2a2ac971237c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118594842"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a>Método IVMFloppyDrive::ReleaseHostDrive

\[Windows O PC virtual não está mais disponível para uso a partir Windows 8. Em vez disso, use o provedor WMI do [Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera uma unidade física no host da unidade de disquete.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Valor/código de retorno                                                                                                                                                          | Descrição                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | A operação foi bem-sucedida.<br/>                                               |
| <dl> <dt>**VM \_ E \_ VM \_ UNKNOWN**</dt> <dt>0xA0040207</dt> </dl>          | A configuração dessa máquina virtual não é válida ou não pode ser encontrada.<br/> |
| <dl> <dt>**VM \_ E \_ MEDIA WRONG TYPE \_ \_ 0XA00400728**</dt> <dt></dt> </dl>  | A mídia anexada a essa unidade de disquete não é uma unidade de disquete física.<br/>     |
| <dl> <dt>**VM \_ E \_ NENHUMA MÍDIA CAPTURADA \_ \_ 0XA00400652**</dt> <dt></dt> </dl> | Não há nenhuma mídia anexada a essa unidade de disquete.<br/>                            |
| <dl> <dt>**DISP \_ E \_ EXCEPTION**</dt> <dt>0x80020009</dt> </dl>          | Ocorreu um erro inesperado.<br/>                                           |



 

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

 

