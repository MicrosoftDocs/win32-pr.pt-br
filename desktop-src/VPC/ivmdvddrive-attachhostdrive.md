---
title: Método IVMDVDDrive AttachHostDrive (VPCCOMInterfaces. h)
description: Anexa uma unidade de host à unidade de DVD na máquina virtual.
ms.assetid: 68e658ba-470c-452c-8124-5bb2ec81911b
keywords:
- AttachHostDrive do método virtual PC
- Método AttachHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método AttachHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c82229488ebb705cab1a684a207f973356d2d43177c4123ae4f456b55fbe6840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136849"
---
# <a name="ivmdvddriveattachhostdrive-method"></a>Método IVMDVDDrive:: AttachHostDrive

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa uma unidade de host à unidade de DVD na máquina virtual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachHostDrive(
  [in] BSTR driveLetter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*letra_da_unidade* \[ no\]
</dt> <dd>

A letra da unidade do host a ser anexada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                    | Descrição                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | A operação foi bem-sucedida.<br/>                                                                                                                                             |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>         | Nenhuma letra de unidade foi especificada ou a letra da unidade especificada é inválida.<br/>                                                                                                  |
| <dl> <dt>**E \_ FALHA**</dt> <dt>0x80004005</dt> </dl>               | Ocorreu um erro inesperado.<br/>                                                                                                                                         |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>    | Não foi possível encontrar a máquina virtual.<br/>                                                                                                                                   |
| <dl> <dt>**VM \_ \_Unidade E \_ em \_ uso**</dt> <dt>0xA0040727</dt> </dl> | Uma unidade de DVD de host ou imagem ISO já está conectada a esta unidade na máquina virtual ou a unidade host especificada já está em uso em outra máquina virtual.<br/> |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl> | O local do barramento desta unidade é inválido ou a unidade não parece ser uma unidade de DVD válida.<br/>                                                                         |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>    | Ocorreu um erro inesperado.<br/>                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Cabeçalho<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

