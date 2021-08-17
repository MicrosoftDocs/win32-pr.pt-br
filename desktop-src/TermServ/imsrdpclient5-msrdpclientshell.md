---
title: Propriedade MsRdpClient5 do IMsRdpClientShell
description: Recupera a interface de configuração do cliente que pode ser escrita por script IMsRdpClientShell.
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota , interface IMsRdpClient5
- Interface IMsRdpClient5 Serviços de Área de Trabalho Remota , propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota , interface IMsRdpClient6
- Interface IMsRdpClient6 Serviços de Área de Trabalho Remota , propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota , interface IMsRdpClient7
- Interface IMsRdpClient7 Serviços de Área de Trabalho Remota , propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota , interface IMsRdpClient8
- Interface IMsRdpClient8 Serviços de Área de Trabalho Remota , propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota , interface IMsRdpClient9
- Interface IMsRdpClient9 Serviços de Área de Trabalho Remota , propriedade MsRdpClientShell
- Propriedade MsRdpClientShell Serviços de Área de Trabalho Remota , interface IMsRdpClient10
- Interface IMsRdpClient10 Serviços de Área de Trabalho Remota , propriedade MsRdpClientShell
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f56b403bb5fd754e95786c2a1d4012ccbbacd3e103b1ee02fbf290ff05d30d3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117942038"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a>Propriedade IMsRdpClient5::MsRdpClientShell

Recupera o [**IMsRdpClientShell**](imsrdpclientshell.md)da interface de configuração de cliente que pode ser scriptável.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro de interface [**IMsRdpClientShell.**](imsrdpclientshell.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClient5 é definido como 4eb5335b-6429-477d-b922-e06a28ecd8bf<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





