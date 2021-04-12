---
title: Propriedade IpAddresses de ITsSbTarget
description: Recupera ou especifica os endereços IP externos do destino.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota da propriedade TargetExternalIpAddresses
- Propriedade TargetExternalIpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Propriedade TargetExternalIpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Propriedade IpAddresses Serviços de Área de Trabalho Remota
- Propriedade IpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTarget
- Serviços de Área de Trabalho Remota de interface ITsSbTarget, Propriedade IpAddresss
- Propriedade IpAddresses Serviços de Área de Trabalho Remota, interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx, Propriedade IpAddresss
topic_type:
- apiref
api_name:
- ITsSbTarget.IpAddresses
- ITsSbTarget.get_IpAddresses
- ITsSbTarget.put_IpAddresses
- ITsSbTargetEx.IpAddresses
- ITsSbTargetEx.get_IpAddresses
- ITsSbTargetEx.put_IpAddresses
- TargetExternalIpAddresses
- ITsSbTarget.TargetExternalIpAddresses
- ITsSbTarget get_TargetExternalIpAddresses
- ITsSbTarget put_TargetExternalIpAddresses
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8b3902840b24bc49ae3bda0510c8355afb67810
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364816"
---
# <a name="itssbtargetipaddresses-property"></a>Propriedade ITsSbTarget:: IpAddresss

Recupera ou especifica os endereços IP externos do destino.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_IpAddresses(
  [in, size_is(numAddresses)]   TSSD_ConnectionPoint *sockaddr,
  [in]                          DWORD                numAddresses
);

HRESULT get_IpAddresses(
  [out, size_is(*numAddresses)] TSSD_ConnectionPoint *sockaddr,
  [in, out]                     DWORD                *numAddresses
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para uma matriz de estruturas [**tssd \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) que recebem os endereços IP externos do destino.

Um ponteiro para uma variável **DWORD** que contém o número de endereços IP externos no parâmetro *SOCKADDR* . Se o número de endereços for desconhecido, passe *SOCKADDR* como **nulo**. O método retornará o número de estruturas [**\_ ConnectionPoint tssd**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessárias para alocar na matriz apontada pelo parâmetro *SOCKADDR* .

## <a name="remarks"></a>Comentários

Essa propriedade era conhecida anteriormente como **TargetExternalIpAddresses** no Windows Server 2008 R2.

Se o número de endereços IP externos for desconhecido, você poderá chamar esse método com *SOCKADDR* definido como **NULL**. O método será retornado, no parâmetro *numAddresses* , o número de estruturas [**\_ ConnectionPoint tssd**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessárias para receber todos os endereços IP externos. Aloque a matriz para *SOCKADDR* com base nesse número e, em seguida, chame o método novamente, configurando *SOCKADDR* para a matriz alocada recentemente e *numAddresses* para o número retornado pela primeira chamada.

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**\_CONNECTIONPOINT tssd**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





