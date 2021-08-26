---
title: Lojas online privadas
description: Lojas online privadas
ms.assetid: c1e241f5-6d29-4b53-8be0-264597e03de7
keywords:
- Windows Media Player lojas online, privadas
- lojas online, privadas
- Digite 1 lojas online, privadas
- tipo 2 lojas online, privadas
- lojas online privadas
- registro, lojas online privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0667c19ffde3bb3c78b539253650e4f6f0b84cfbfd940f4d06237f987b99efd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002926"
---
# <a name="private-online-stores"></a>Lojas online privadas

o Windows Media Player 10 ou posterior dá suporte a lojas online privadas; ou seja, os armazenamentos que são visíveis apenas para determinados usuários. Para que um repositório online privado fique visível para o usuário atual, deve haver uma entrada que represente a loja online privada na seguinte chave do registro.

HKEY \_ atual \_ software de usuário \\ \\ Microsoft \\ MediaPlayer \\ PrivateServices

A entrada de registro necessária deve ter o seguinte formato.



| Nome                                                         | Tipo           | Valor                                                                     |
|--------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| Qualquer nome escolhido pela pessoa que cria a entrada do registro | **REG \_ DWORD** | Um número, fornecido pela Microsoft, que identifica a loja online privada |



 

o controle Windows Media Player 10 ActiveX dá suporte a lojas online privadas somente se o controle estiver sendo executado no modo remoto. o controle Windows Media Player 11 ActiveX dá suporte a lojas online privadas, independentemente de o controle estar sendo executado no modo remoto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




