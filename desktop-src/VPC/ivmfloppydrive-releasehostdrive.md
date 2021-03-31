---
title: Método IVMFloppyDrive ReleaseHostDrive (VPCCOMInterfaces. h)
description: Libera uma unidade física no host da unidade de disquete.
ms.assetid: 6d5a8e7c-684c-42bc-84e5-76d3e761b7f0
keywords:
- ReleaseHostDrive do método virtual PC
- Método ReleaseHostDrive Virtual PC, interface IVMFloppyDrive
- IVMFloppyDrive interface virtual PC, método ReleaseHostDrive
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
ms.openlocfilehash: a4ab726ba87dd978a21c4f27b20437926e07c19b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644217"
---
# <a name="ivmfloppydrivereleasehostdrive-method"></a>Método IVMFloppyDrive:: ReleaseHostDrive

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Libera uma unidade física no host da unidade de disquete.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT ReleaseHostDrive();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código/valor de retorno                                                                                                                                                          | Description                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0</dt> </dl>                                | A operação foi bem-sucedida.<br/>                                               |
| <dl> <dt>**VM \_ E 0xA0040207 de \_ VM \_ desconhecido**</dt> <dt></dt> </dl>          | A configuração desta máquina virtual não é válida ou não foi encontrada.<br/> |
| <dl> <dt>**VM \_ \_Mídia E \_ \_ tipo incorreto**</dt> <dt>0xA00400728</dt> </dl>  | A mídia anexada a esta unidade de disquete não é uma unidade de disquete física.<br/>     |
| <dl> <dt>**VM \_ E \_ nenhuma \_ mídia \_ capturada**</dt> <dt>0xA00400652</dt> </dl> | Não há mídia anexada a esta unidade de disquete.<br/>                            |
| <dl> <dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção </dl>          | Ocorreu um erro inesperado.<br/>                                           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMFloppyDrive é definido como 661abee6-112a-4ed9-babf-3c874969f10e<br/>             |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**IVMFloppyDrive**](ivmfloppydrive.md)
</dt> </dl>

 

