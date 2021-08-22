---
title: Associação tardia versus acesso Vtable no modelo de extensão ADSI
description: Uma interface dupla permite o acesso direto à vtable a todas as suas funções, enquanto uma interface de expedição não.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- associação tardia versus acesso vtable no ADSI do modelo de extensão ADSI
- extensões ADSI, associação tardia versus acesso vtable no modelo de extensão ADSI
- ADSI ADSI , código de exemplo Visual Basic , usando IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8eacc2008d3da33cd8d1897eeff2c30301849f9ec306656fc494072c33608c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023354"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Associação tardia versus acesso Vtable no modelo de extensão ADSI

Uma interface dupla permite o acesso direto à vtable a todas as suas funções, enquanto uma interface de expedição não. Um cliente C/C++ pode consultar um ponteiro de interface dupla e usar o acesso direto à vtable para invocar suas funções. Isso fornece acesso mais rápido do que invocar a função usando as funções [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch::Invoke.**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) Isso é especialmente verdadeiro no modelo de extensão, porque todas as interfaces duplas em um objeto de extensão devem delegar suas funções **GetIDsOfNames** e **Invoke** de volta ao ADSI (agregador) primeiro. Em seguida, o agregador deve executar etapas internas extras para identificar qual objeto de extensão, possivelmente incluindo o próprio agregador, fornece suporte para a função chamada e redireciona a chamada para o objeto apropriado.

Visual Basic também invoca uma função de interface dupla usando o acesso direto a uma vtable, se ela tiver um ponteiro para a interface e acesso aos dados de tipo da biblioteca de tipos. Os clientes ADSI escritos em Visual Basic podem especificar um ponteiro para uma interface dupla, por exemplo, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitamente e, portanto, habilitar o acesso vtable a funções na interface.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Como uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) não dá suporte ao acesso vtable, este exemplo não se aplica. Ou seja, uma função de expedição sempre é invocada por meio das funções [**IDispatch::GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch::Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) somente.

As versões atuais do VBScript e JScript também não têm suporte para acesso vtable. Portanto, uma interface dupla em um ambiente VBScript ou JScript executa como uma interface de expedição.

 

 