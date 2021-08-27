---
title: Propriedade ITsSbTarget IpAddresses
description: Recupera ou especifica os endereços IP externos do destino.
ms.assetid: 938a753c-d541-4772-b41b-817324488685
ms.tgt_platform: multiple
keywords:
- Propriedade TargetExternalIpAddresses Serviços de Área de Trabalho Remota
- Propriedade TargetExternalIpAddresses Serviços de Área de Trabalho Remota interface , ITsSbTarget
- Propriedade TargetExternalIpAddresses Serviços de Área de Trabalho Remota interface , ITsSbTarget
- Propriedade IpAddresses Serviços de Área de Trabalho Remota
- Propriedade IpAddresses Serviços de Área de Trabalho Remota interface , ITsSbTarget
- Interface ITsSbTarget Serviços de Área de Trabalho Remota propriedade , IpAddresses
- Propriedade IpAddresses Serviços de Área de Trabalho Remota , interface ITsSbTargetEx
- Interface ITsSbTargetEx Serviços de Área de Trabalho Remota , propriedade IpAddresses
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
ms.openlocfilehash: 21afd8d2349bfef37dcc39b684c3f5b837728f79
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122988269"
---
# <a name="itssbtargetipaddresses-property"></a>Propriedade ITsSbTarget::IpAddresses

Recupera ou especifica os endereços IP externos do destino.

Essa propriedade é leitura/gravação.

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

Um ponteiro para uma matriz de [**estruturas do \_ ConnectionPoint TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) que recebem os endereços IP externos do destino.

Um ponteiro para uma **variável DWORD** que contém o número de endereços IP externos no *parâmetro sockaddr.* Se o número de endereços for desconhecido, passe *sockaddr* como **NULL.** O método retornará o número de estruturas [**TSSD \_ ConnectionPoint**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessárias para alocar na matriz apontada pelo *parâmetro sockaddr.*

## <a name="remarks"></a>Comentários

Essa propriedade era anteriormente conhecida como **TargetExternalIpAddresses** no Windows Server 2008 R2.

Se o número de endereços IP externos for desconhecido, você poderá chamar esse método com *sockaddr* definido como **NULL.** Em seguida, o método retornará, no *parâmetro numAddresses,* o número de estruturas [**do \_ ConnectionPoint TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint) necessárias para receber todos os endereços IP externos. Aloce a matriz para *sockaddr* com base nesse número e chame o método novamente, definindo *sockaddr* como a matriz recém-alocada e *numAddresses* como o número retornado pela primeira chamada.

## <a name="requirements"></a>Requisitos




| Requisito | Valor |
|--------|-------|
| Cliente mínimo com suporte<br /> | Nenhum compatível<br /> | 
| Servidor mínimo com suporte<br /> | Windows Server 2012<br /> | 
| IDL<br /> | <dl><dt>Sbtsv.idl</dt></dl> | 
| IID<br /> | IID_ITsSbTarget é definido como:<ul><li>16616ECC-272D-411D-B324-126893033856</li><li>e85e10ea-db0b-4752-b456-5fd5840901c0 no Windows Server 2008 R2</li></ul> | 




## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ITsSbTargetEx**](itssbtargetex.md)
</dt> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[**ConnectionPoint do \_ TSSD**](/windows/win32/api/sessdirpublictypes/ns-sessdirpublictypes-tssd_connectionpoint)
</dt> </dl>

 

 





