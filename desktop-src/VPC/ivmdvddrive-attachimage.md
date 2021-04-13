---
title: Método IVMDVDDrive AttachImage (VPCCOMInterfaces. h)
description: Anexa uma imagem ISO à unidade de DVD na VM.
ms.assetid: 08947898-ca3f-41b6-97a3-52dc6977fc6d
keywords:
- AttachImage do método virtual PC
- Método AttachImage Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método AttachImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.AttachImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58204545e21bd7dbf48d21acbc232b9fc5d1e3b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369862"
---
# <a name="ivmdvddriveattachimage-method"></a>Método IVMDVDDrive:: AttachImage

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Anexa uma imagem ISO à unidade de DVD na VM (máquina virtual).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT AttachImage(
  [in] BSTR imagePath
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*imagePath* \[ no\]
</dt> <dd>

O caminho completo para a imagem ISO que deve ser anexada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                    | Descrição                                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                          | A operação foi bem-sucedida.<br/>                                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt> </dl>         | O parâmetro *imagePath* é um diretório.<br/>                                                         |
| <dl> <dt>**E \_**</dt> <dt>0X80004003</dt> de ponteiro </dl>            | O parâmetro *imagePath* é **nulo**.<br/>                                                            |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>    | Não foi possível encontrar a VM.<br/>                                                                        |
| <dl> <dt>**VM \_ \_Unidade E \_ em \_ uso**</dt> <dt>0xA0040727</dt> </dl> | Uma unidade de DVD de host ou imagem ISO já está conectada a esta unidade.<br/>                                  |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl> | O local do barramento desta unidade é inválido ou a unidade não parece ser uma unidade de DVD válida.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>    | Ocorreu um erro inesperado.<br/>                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDVDDrive é definido como b96328f6-6732-437d-a00d-ffa47e43971c<br/>                |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IVMDVDDrive**](ivmdvddrive.md)
</dt> </dl>

 

