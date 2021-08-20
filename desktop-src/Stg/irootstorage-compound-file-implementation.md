---
title: IRootStorage – Implementação de arquivo composto
description: A implementação de arquivo composto do COM de IRootStorage permite que você suporte a salvar arquivos em situações de memória baixa ou de espaço em disco baixo. Para obter informações sobre como essa interface se comporta, consulte IRootStorage.
ms.assetid: 0847929e-63ce-42f9-9d47-2e7222e003bb
keywords:
- IRootStorage Strctd Stg , implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20128e749443d19c6418703bf64d93eb763ae25103d677719bb4cb4cd21349a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961194"
---
# <a name="irootstorage---compound-file-implementation"></a>IRootStorage – Implementação de arquivo composto

A implementação de arquivo composto do [**COM de IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) permite que você suporte a salvar arquivos em situações de memória baixa ou de espaço em disco baixo. Para obter informações sobre como essa interface se comporta, consulte **IRootStorage**.

## <a name="when-to-use"></a>Quando usar

Use a implementação fornecida pelo sistema de [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) somente para dar suporte à salvação de arquivos em condições de memória baixa.

## <a name="remarks"></a>Comentários

É possível chamar a implementação de COM de [**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile) para fazer uma operação de salvar como normal para outro arquivo. No entanto, os aplicativos que fazem isso podem não ser compatíveis com gerações futuras de armazenamento COM. Para evitar essa possibilidade, os aplicativos que executam uma operação de salvar como devem criar manualmente o segundo arquivo composto e invocar [**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto). O **método IRootStorage::SwitchToFile** deve ser usado somente em situações de emergência (memória baixa ou espaço em disco).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Irootstorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IRootStorage::SwitchToFile**](/windows/desktop/api/Objidl/nf-objidl-irootstorage-switchtofile)
</dt> </dl>

 

 




