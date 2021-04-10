---
title: Páginas de código e cadeias de caracteres Unicode
description: Outra consideração na implementação de IPropertySetStorage é como os nomes de propriedade Unicode são armazenados na ID de propriedade 0 (o dicionário de nome de propriedade), que não usa cadeias de caracteres Unicode.
ms.assetid: 830c90c9-d2a5-4ecf-8cb6-9950ed5320bf
keywords:
- Páginas de código e cadeias de caracteres Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 508d508ec21e7e763a683e534cf485ebbeec018d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291869"
---
# <a name="code-pages-and-unicode-strings"></a>Páginas de código e cadeias de caracteres Unicode

Outra consideração na implementação de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) é como os nomes de propriedade Unicode são armazenados na ID de propriedade 0 (o dicionário de nome de propriedade), que não usa cadeias de caracteres Unicode.

O Unicode oficialmente tem um valor de página de código de 1200. Para armazenar valores Unicode no dicionário de nome de propriedade, use um valor de página de código de 1200 para o conjunto de propriedades inteiro (na propriedade ID 1), especificado pela ausência do sinalizador **\_ ANSI PROPSETFLAG** em [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Lembre-se de que isso tem o efeito colateral de armazenar todos os valores de cadeia de caracteres na propriedade definida em Unicode. Em todas as páginas de código, a contagem encontrada no início de um **VT \_ LPSTR** é uma contagem de bytes, não uma contagem de caracteres. Isso é necessário para fornecer compatibilidade com clientes de versão anterior.

A implementação do arquivo composto de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) cria todos os novos conjuntos de propriedades totalmente em Unicode (página de código 1200) ou na página de código ANSI do sistema atual. Isso é controlado pela ausência ou presença do sinalizador **\_ ANSI PROPSETFLAG** no parâmetro *grfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create).

Crie e abra conjuntos de propriedades como Unicode. Para implementar isso, não defina o sinalizador **\_ ANSI PROPSETFLAG** no parâmetro *grfFlags* de [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create). Evite usar valores de ' **VT \_ LPSTR** ' e, em vez disso, usar valores de do **VT \_** . Quando a página de código do conjunto de propriedades é Unicode, os valores da cadeia de caracteres **VT \_ LPSTR** são convertidos em Unicode quando armazenados e de volta para valores de cadeia de caracteres multibyte quando recuperados.

Definir o **sinalizador \_ ANSI PROPSETFLAG** como relatado por meio de uma chamada para [**IPropertyStorage:: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat) reflete se a página de código subjacente é ou não Unicode. Lembre-se de que a ID de propriedade 1 pode ser lida explicitamente para aprender a página de código.

Você pode acessar a ID de propriedade 1 por meio de uma chamada para [**IPropertyStorage:: ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple). No entanto, ele é somente leitura e não pode ser atualizado com [**WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple). Além disso, ele não pode ser excluído com [**DeleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple).

 

 




