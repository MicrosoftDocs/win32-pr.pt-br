---
title: PreferredServerBitness
description: Define a arquitetura preferida, 32 bits ou 64 bits, para esse servidor COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- COM valor do registro PreferredServerBitness COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b003fd4bdd861cbfd82e249123831e4e017eaeef1ad76b95121244fd415ae0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118309981"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

Define a arquitetura preferida, 32 bits ou 64 bits, para esse servidor COM.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Comentários

Esse é um valor **reg \_ DWORD** que está disponível apenas nas versões de 64 bits do Windows.



| Valor | Descrição                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Corresponder a arquitetura do servidor à arquitetura do cliente. Por exemplo, se o cliente for de 32 bits, use uma versão de 32 bits do servidor, se estiver disponível. Caso contrário, a solicitação de ativação do cliente falhará. |
| 2     | Use uma versão de 32 bits do servidor. Se não houver um, a solicitação de ativação do cliente falhará.                                                                                                      |
| 3     | Use uma versão de 64 bits do servidor. Se não houver um, a solicitação de ativação do cliente falhará.                                                                                                      |



 

Se esse valor não estiver presente, então:

-   se o computador que hospeda o servidor estiver executando Windows XP ou Windows server 2003 sem SP1 ou posterior instalado, o COM prefere uma versão de 64 bits do servidor, se disponível; caso contrário, ele ativará uma versão de 32 bits do servidor.
-   se o computador que hospeda o servidor estiver executando o Windows server 2003 com SP1 ou posterior estiver instalado, o COM tentará corresponder a arquitetura do servidor à arquitetura do cliente. Em outras palavras, para um cliente de 32 bits, o COM ativará um servidor de 32 bits, se disponível; caso contrário, ele ativará uma versão de 64 bits do servidor. Para um cliente de 64 bits, o COM ativará um servidor de 64 bits, se disponível; caso contrário, ele ativará um servidor de 32 bits.

O cliente também pode especificar sua própria preferência de arquitetura por meio dos sinalizadores de servidor CLSCTX \_ Activate de \_ 32 \_ bits \_ e CLSCTX \_ Ativar \_ 64 \_ bits \_ , e eles substituirão a preferência do servidor. Para obter mais informações e um gráfico de possíveis interações entre as preferências de arquitetura do cliente e do servidor, consulte [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 