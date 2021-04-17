---
title: Monikers de arquivo
description: Monikers de arquivo
ms.assetid: 923f798d-d789-4e6d-b27e-dd5a72f92abf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5c18beeff04804b11f04c0a2c211f2dd09dd60d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291986"
---
# <a name="file-monikers"></a>Monikers de arquivo

Os *monikers de arquivo* são a classe de moniker mais simples. Os identificadores de arquivo podem ser usados para identificar qualquer objeto armazenado em seu próprio arquivo. Um moniker de arquivo atua como um wrapper para o nome do caminho que o sistema de arquivos nativo atribui ao arquivo. Chamar [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) para esse moniker faria com que esse objeto fosse ativado e, em seguida, retornaria um ponteiro de interface para o objeto. A origem do objeto nomeado pelo moniker deve fornecer uma implementação da interface [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile) para dar suporte à associação de um moniker de arquivo. Os monikers de arquivo podem representar um caminho completo ou relativo.

Por exemplo, o moniker do arquivo para um objeto de planilha armazenado como o arquivo C: \\ Work \\MySheet.xls conteria informações equivalentes a esse nome de caminho. No entanto, o moniker não consistiria necessariamente na mesma cadeia de caracteres. A cadeia de caracteres é apenas seu *nome displayÂ*, uma representação do conteúdo do moniker que é significativo para um usuário final. O nome de exibição, que está disponível por meio do método [**IMoniker:: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) , é usado somente ao exibir um moniker para um usuário final. Esse método obtém o nome de exibição para qualquer uma das classes de moniker. Internamente, o moniker pode armazenar as mesmas informações em um formato mais eficiente para executar operações de moniker, mas não é significativo para os usuários. Em seguida, quando esse mesmo objeto é vinculado por meio de uma chamada para o método [**BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) , o objeto seria ativado, provavelmente carregando o arquivo na planilha.

O OLE oferece aos provedores de moniker a função auxiliar [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) que cria um objeto de moniker de arquivo e retorna seu ponteiro para o provedor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Anti-moniker](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers compostos](composite-monikers.md)
</dt> <dt>

[Monikers de item](item-monikers.md)
</dt> <dt>

[Monikers de ponteiro](pointer-monikers.md)
</dt> </dl>

 

 




