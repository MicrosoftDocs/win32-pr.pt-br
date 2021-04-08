---
description: Define valores que determinam como buscar a credencial de uma conta de serviço gerenciado de grupo (gMSA).
ms.assetid: 90891448-22F6-497A-A612-3DAB8622C325
title: Enumeração de CRED_FETCH (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRED_FETCH
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 6a7c30f29826b017bc7a3badd796955ec31a1ca7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922239"
---
# <a name="cred_fetch-enumeration"></a>Enumeração de busca de credenciais \_

Define valores que determinam como buscar a credencial de uma conta de serviço gerenciado de grupo (gMSA).

## <a name="syntax"></a>Syntax


```C++
typedef enum _CRED_FETCH { 
  CredFetchDefault  = 0,
  CredFetchDPAPI    = 1,
  CredFetchForced   = 2
} CRED_FETCH;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span>**CredFetchDefault**
</dt> <dd>

Significa que o sistema operacional deve primeiro tentar recuperar a senha do cache local. Se for o momento de buscar a senha, o sistema operacional deverá contatar um controlador de domínio para a senha. Se isso falhar, retorne todas as senhas em cache com o valor de status êxito.

</dd> <dt>

<span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span>**CredFetchDPAPI**
</dt> <dd>

Retorna a credencial DPAPI local para o chamador. Os SSPs ( [*provedores de suporte de segurança*](/windows/desktop/SecGloss/s-gly) ) geralmente não exigem o uso dessa enumeração.

</dd> <dt>

<span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span>**CredFetchForced**
</dt> <dd>

Força o sistema operacional a tentar ler a senha do controlador de domínio. Durante a hora de substituição da senha, a senha pode ter sido alterada no controlador de domínio e em outros hosts membros, mas o host membro do gMSA reconhece a senha como ainda válida. Isso pode acontecer devido a problemas de distorção de relógio entre diferentes controladores de domínio. Quando esse valor é especificado, o sistema operacional determina se pode haver uma possível alteração de senha devido à distorção do relógio e, nesse caso, recupera a senha. Caso contrário, a credencial armazenada em cache será retornada. Se não houver nenhuma credencial armazenada em cache, o sistema operacional tentará obter uma do controlador de domínio.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

