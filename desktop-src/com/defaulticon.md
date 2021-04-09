---
title: DefaultIcon
description: Fornece informações de ícone padrão para icônico apresentações de objetos.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008419"
---
# <a name="defaulticon"></a>DefaultIcon

Fornece informações de ícone padrão para icônico apresentações de objetos.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a>Comentários

Esse é um valor **reg \_ sz** que especifica o caminho completo para o nome do executável do aplicativo de objeto e o índice de recursos do ícone no executável.

**DefaultIcon** identifica o ícone a ser usado quando, por exemplo, um controle é minimizado para um ícone. Essa entrada contém o caminho completo para o nome do executável do aplicativo de servidor e o índice de recursos do ícone no executável. Os aplicativos podem usar as informações fornecidas por **DefaultIcon** para obter um identificador de ícone com [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).

 

 