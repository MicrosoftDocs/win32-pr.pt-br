---
title: Propriedade IMsRdpClientShell RdpFileContents
description: Especifica ou recupera o conteúdo do arquivo de protocolo RDP (RDP) a ser iniciado a partir de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de algum outro portal da Web.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade RdpFileContents
- Propriedade RdpFileContents Serviços de Área de Trabalho Remota, interface IMsRdpClientShell
- Serviços de Área de Trabalho Remota de interface IMsRdpClientShell, Propriedade RdpFileContents
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105789436"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a>Propriedade IMsRdpClientShell:: RdpFileContents

Especifica ou recupera o conteúdo do arquivo de protocolo RDP (RDP) a ser iniciado a partir de Acesso via Web à Área de Trabalho Remota (RD Acesso via Web) ou de algum outro portal da Web.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a>Valor da propriedade

Especifica o conteúdo do arquivo RDP a ser iniciado no portal da Web.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell é definido como d012ae6d-c19a-4bfe-B367-201f8911f134<br/>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





