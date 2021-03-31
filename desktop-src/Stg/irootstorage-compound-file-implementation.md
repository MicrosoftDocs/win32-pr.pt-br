---
title: IRootStorage-implementação de arquivo composto
description: A implementação de arquivo composto do COM do IRootStorage permite que você dê suporte ao salvamento de arquivos em situações de baixa memória ou pouco espaço em disco. Para obter informações sobre como essa interface se comporta, consulte IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928f78e88ffaa526006c0a33e803076db0ec301e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637258"
---
# <a name="irootstorage---compound-file-implementation"></a>IRootStorage-implementação de arquivo composto

A implementação de arquivo composto do COM do [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) permite que você dê suporte ao salvamento de arquivos em situações de baixa memória ou pouco espaço em disco. Para obter informações sobre como essa interface se comporta, consulte **IRootStorage**.

## <a name="when-to-use"></a>Quando usar

Use a implementação fornecida pelo sistema do [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) apenas para dar suporte ao salvamento de arquivos em condições de baixa memória.

## <a name="remarks"></a>Comentários

É possível chamar a implementação de COM de [**IRootStorage:: SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) para fazer uma operação salvar como normal em outro arquivo. No entanto, os aplicativos que fazem isso podem não ser compatíveis com gerações futuras do armazenamento COM. Para evitar essa possibilidade, os aplicativos que executam uma operação salvar como devem criar manualmente o segundo arquivo composto e invocar [**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). O método **IRootStorage:: SwitchToFile** deve ser usado somente em situações de emergência (memória insuficiente ou de espaço em disco).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




