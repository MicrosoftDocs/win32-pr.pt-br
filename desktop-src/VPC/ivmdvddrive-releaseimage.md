---
title: Método IVMDVDDrive ReleaseImage (VPCCOMInterfaces. h)
description: Libera uma imagem ISO capturada da unidade de DVD.
ms.assetid: 7cc95cf3-9d25-495f-863c-8eddd4068835
keywords:
- ReleaseImage do método virtual PC
- Método ReleaseImage Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método ReleaseImage
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a36a13b258d155760269399d9f25f5eda6f296
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454723"
---
# <a name="ivmdvddrivereleaseimage-method"></a>Método IVMDVDDrive:: ReleaseImage

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera uma imagem ISO capturada da unidade de DVD.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseImage();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                         | Descrição                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                               | A operação foi bem-sucedida.<br/>                                      |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>         | Não foi possível encontrar a máquina virtual.<br/>                            |
| <dl> <dt>**VM \_ \_Mídia E \_ \_ tipo incorreto**</dt> <dt>0xA00400728</dt> </dl> | A mídia capturada atualmente não é uma unidade de disco de host.<br/>             |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl>      | A unidade não pôde ser inicializada devido a um local de barramento inválido.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>         | Ocorreu um erro inesperado.<br/>                                  |



 

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

 

