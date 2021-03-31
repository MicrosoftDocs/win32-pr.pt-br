---
title: Propriedade Farmname de ITsSbTarget
description: Recupera ou especifica o nome do farm ao qual esse destino está associado.
ms.assetid: 83e168ae-f985-40f9-912b-496c0695f82a
ms.tgt_platform: multiple
keywords:
- Propriedade farmname Serviços de Área de Trabalho Remota
- Propriedade farmname Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade Farmname
- Propriedade farmname Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade Farmname
topic_type:
- apiref
api_name:
- ITsSbTarget.FarmName
- ITsSbTarget.get_FarmName
- ITsSbTarget.put_FarmName
- ITsSbTargetEx.FarmName
- ITsSbTargetEx.get_FarmName
- ITsSbTargetEx.put_FarmName
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94f86b2cf0ec257be9fe9b801e6fceae364a46e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103638508"
---
# <a name="itssbtargetfarmname-property"></a>Propriedade ITsSbTarget:: Farmname

Recupera ou especifica o nome do farm ao qual esse destino está associado.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT put_FarmName(
  [in]          BSTR Val
);

HRESULT get_FarmName(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Uma variável **BSTR** que contém o nome do farm.

## <a name="requirements"></a>Requisitos



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Cliente mínimo com suporte<br/></td>
<td>Nenhum compatível<br/></td>
</tr>
<tr class="even">
<td>Servidor mínimo com suporte<br/></td>
<td>Windows Server 2012<br/></td>
</tr>
<tr class="odd">
<td>INSERI<br/></td>
<td><dl> <dt>Sbtsv. idl</dt> </dl></td>
</tr>
<tr class="even">
<td>IID<br/></td>
<td>IID_ITsSbTarget é definido como:
<ul>
<li>16616ECC-272D-411D-B324-126893033856</li>
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 no Windows Server 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





