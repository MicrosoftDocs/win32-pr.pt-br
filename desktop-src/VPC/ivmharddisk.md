---
title: Interface IVMHardDisk (VPCCOMInterfaces. h)
description: Fornece acesso a uma imagem de disco rígido. Ele pode ser acessado por meio da propriedade IVMHardDiskConnection HD ou do método IVMVirtualPC GetHardDisk.
ms.assetid: 0c536906-91be-428a-8199-c452abef423d
keywords:
- Virtual PC de interface IVMHardDisk
- Virtual PC de interface IVMHardDisk, descrito
topic_type:
- apiref
api_name:
- IVMHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24d6df46e7c698676e3873dd17a854fd0b7d7933
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454587"
---
# <a name="ivmharddisk-interface"></a>Interface IVMHardDisk

\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8. Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Fornece acesso a uma imagem de disco rígido. Ele pode ser acessado por meio da propriedade [**IVMHardDiskConnection:: HD**](ivmharddiskconnection-harddisk.md) ou do método [**IVMVirtualPC:: GetHardDisk**](ivmvirtualpc-getharddisk.md) .

## <a name="members"></a>Membros

A interface **IVMHardDisk** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHardDisk** também tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A interface **IVMHardDisk** tem esses métodos.



| Método                                 | Descrição                                                                                                                                                 |
|:---------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compacto**](ivmharddisk-compact.md) | Compacta uma imagem de disco rígido virtual de expansão dinâmica.<br/>                                                                                        |
| [**Converter**](ivmharddisk-convert.md) | Converte qualquer disco rígido virtual em um disco rígido virtual de expansão dinâmica ou em um disco rígido virtual de tamanho fixo.<br/>                            |
| [**Mescle**](ivmharddisk-merge.md)     | Mescla um disco rígido virtual diferencial com sua imagem de disco pai.<br/>                                                                              |
| [**Mesclar**](ivmharddisk-mergeto.md) | Mescla um disco rígido virtual diferencial com todos os seus pais (até e incluindo o disco rígido virtual pai raiz) em um novo arquivo de disco rígido.<br/> |



 

### <a name="properties"></a>Propriedades

A interface **IVMHardDisk** tem essas propriedades.



| Propriedade                                                              | Tipo de acesso           | Descrição                                                                                    |
|:----------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Arquivo**](ivmharddisk-file.md)<br/>                           | Somente leitura<br/>  | O nome do caminho completo do arquivo de disco rígido virtual.<br/>                                   |
| [**HostFreeDiskSpace**](ivmharddisk-hostfreediskspace.md)<br/> | Somente leitura<br/>  | A quantidade de espaço em disco restante disponível no host para o disco rígido virtual.<br/> |
| [**Pai**](ivmharddisk-parent.md)<br/>                       | Leitura/gravação<br/> | O pai do disco rígido virtual diferencial.<br/>                                   |
| [**SizeInGuest**](ivmharddisk-sizeinguest.md)<br/>             | Somente leitura<br/>  | O tamanho do disco rígido virtual no sistema operacional convidado.<br/>                    |
| [**SizeOnHost**](ivmharddisk-sizeonhost.md)<br/>               | Somente leitura<br/>  | O tamanho do arquivo de disco rígido virtual no computador host.<br/>                        |
| [**Tipo**](ivmharddisk-type.md)<br/>                           | Somente leitura<br/>  | O tipo do disco rígido virtual.<br/>                                                  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                     |
| Fim do suporte do cliente<br/>    | Windows 7<br/>                                                                          |
| Produto<br/>                  | Windows Virtual PC<br/>                                                                 |
| parâmetro<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHardDisk é definido como ffa14ae6-48f5-42a4-8a22-186f2e5c7db0<br/>                |



 

