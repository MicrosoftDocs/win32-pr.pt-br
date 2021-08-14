---
title: Propriedade ITsSbTarget TargetLoad
description: Recupera a carga relativa em um destino.
ms.assetid: 56618dcf-1319-4310-80ba-7ed71b8b02e8
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TargetLoad
- Propriedade TargetLoad Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade TargetLoad
- Propriedade TargetLoad Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade TargetLoad
topic_type:
- apiref
api_name:
- ITsSbTarget.TargetLoad
- ITsSbTarget.get_TargetLoad
- ITsSbTargetEx.TargetLoad
- ITsSbTargetEx.get_TargetLoad
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c367e9c00caff78bb3e64263c1622de45fa6e640e78d88239e1ed25a6f68558
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989856"
---
# <a name="itssbtargettargetload-property"></a>Propriedade ITsSbTarget:: TargetLoad

Recupera a carga relativa em um destino. Esse valor é baseado no número de sessões existentes e pendentes. Por padrão, uma sessão pendente tem o mesmo valor de uma sessão existente.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_TargetLoad(
  [out, retval] DWORD *pTargetLoad
);
```



## <a name="property-value"></a>Valor da propriedade

Um número que representa a carga relativa em um destino.

## <a name="remarks"></a>Comentários

O peso de uma sessão pendente em relação a uma sessão ativa pode ser alterado definindo o valor do parâmetro *\_ ConnectionEstablishmentPenalty de lb* para o agente de conexão. Esse parâmetro está localizado na chave do registro **HKLM \\ System \\ CurrentControlSet \\ Services \\ Tssdis \\ Parameters** . O valor padrão de 1 especifica que as sessões pendentes têm o mesmo peso que as sessões ativas.

essa propriedade está disponível no Windows Server 2012 R2 com [KB3091411](https://support.microsoft.com/kb/3091411) instalado na interface [**ITsSbTargetEx**](itssbtargetex.md) .

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
<td>Windows Server 2016<br/></td>
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
<li>e85e10ea-db0b-4752-b456-5fd5840901c0 no servidor Windows 2008 R2</li>
</ul></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> </dl>

 

 





