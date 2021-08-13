---
description: A ação RegisterUser registra as informações do usuário com o instalador para identificar o usuário de um produto.
ms.assetid: da615cb4-d36d-4180-8f97-c9f83c0df1c6
title: Ação RegisterUser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89d43d18839e806939b7a084d37840b9895fdc81efb79fc03867eebe4c5c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118626711"
---
# <a name="registeruser-action"></a>Ação RegisterUser

A ação RegisterUser registra as informações do usuário com o instalador para identificar o usuário de um produto.

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação   |
|-------|------------------------------|
| \[1\] | Informações de usuário registradas. |



 

## <a name="remarks"></a>Comentários

A ação RegisterUser não é executada durante uma instalação administrativa. Se o identificador do produto inserido pelo usuário não tiver sido validado pela [ação ValidateProductID](validateproductid-action.md), a propriedade [**ProductID**](productid.md) não será definida e essa ação não fará nada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**USU**](username.md)
</dt> <dt>

[**COMPANYNAME**](companyname.md)
</dt> <dt>

[**ProductID**](productid.md)
</dt> </dl>

 

 



