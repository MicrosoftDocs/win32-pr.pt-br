---
title: Método IVMDVDDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libera uma unidade de host capturada da unidade de DVD.
ms.assetid: 88bbe364-0c39-40c2-89e7-22ffd66259a2
keywords:
- ReleaseHostDrive do método virtual PC
- Método ReleaseHostDrive Virtual PC, interface IVMDVDDrive
- IVMDVDDrive interface virtual PC, método ReleaseHostDrive
topic_type:
- apiref
api_name:
- IVMDVDDrive.ReleaseHostDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 865b9aa54304d8ddacacf048825d6c9767347f341d31524cbd4dd60d7060ae4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119136799"
---
# <a name="ivmdvddrivereleasehostdrive-method"></a>Método IVMDVDDrive:: ReleaseHostDrive

\[Windows O Virtual PC não está mais disponível para uso a partir de Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera uma unidade de host capturada da unidade de DVD.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                         | Descrição                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                               | A operação foi bem-sucedida.<br/>                                      |
| <dl> <dt>**E \_ FALHA**</dt> <dt>0x80004005</dt> </dl>                    | Ocorreu um erro inesperado.<br/>                                  |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>         | Não foi possível encontrar a máquina virtual.<br/>                            |
| <dl> <dt>**VM \_ \_Mídia E \_ \_ tipo incorreto**</dt> <dt>0xA00400728</dt> </dl> | A mídia capturada atualmente não é uma unidade de disco de host.<br/>             |
| <dl> <dt>**VM \_ Unidade E 0xA0040502 \_ \_ inválidas**</dt> <dt></dt> </dl>      | A unidade não pôde ser inicializada devido a um local de barramento inválido.<br/> |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>         | Ocorreu um erro inesperado.<br/>                                  |



 

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

 

