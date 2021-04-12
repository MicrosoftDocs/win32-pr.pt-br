---
title: Lojas online privadas
description: Lojas online privadas
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Armazenamentos online do Windows Media Player, privado
- lojas online, privadas
- Digite 1 lojas online, privadas
- tipo 2 lojas online, privadas
- lojas online privadas
- registro, lojas online privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e11490a8a12659dfc1e2c5445167e8d71abaf00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364187"
---
# <a name="private-online-stores"></a>Lojas online privadas

O Windows Media Player 10 ou posterior dá suporte a lojas online privadas; ou seja, os armazenamentos que são visíveis apenas para determinados usuários. Para que um repositório online privado fique visível para o usuário atual, deve haver uma entrada que represente a loja online privada na seguinte chave do registro.

HKEY \_ atual \_ software de usuário \\ \\ Microsoft \\ MediaPlayer \\ PrivateServices

A entrada de registro necessária deve ter o seguinte formato.



| Nome                                                         | Tipo           | Valor                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Qualquer nome escolhido pela pessoa que cria a entrada do registro | **REG \_ DWORD** | Um número, fornecido pela Microsoft, que identifica a loja online privada |



 

O controle ActiveX do Windows Media Player 10 dá suporte a lojas online privadas somente se o controle estiver sendo executado no modo remoto. O controle ActiveX do Windows Media Player 11 dá suporte a lojas online privadas, independentemente de o controle estar sendo executado no modo remoto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




