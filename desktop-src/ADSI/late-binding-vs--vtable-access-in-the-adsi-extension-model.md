---
title: Associação tardia versus acesso de vtable no modelo de extensão ADSI
description: Uma interface dupla habilita o acesso Direct vtable a todas as suas funções, enquanto uma interface de expedição não.
ms.assetid: 6ecc0821-7cf0-4075-81c0-8bebaedab2a4
ms.tgt_platform: multiple
keywords:
- vinculação tardia versus acesso vtable no ADSI do modelo de extensão ADSI
- ADSI de extensões, associação tardia versus acesso vtable no modelo de extensão ADSI
- ADSI ADSI, código de exemplo Visual Basic, usando IADsDualInf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f95431fcde9a194f28cd103d93faa3f182c1968
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105762843"
---
# <a name="late-binding-vs-vtable-access-in-the-adsi-extension-model"></a>Associação tardia versus acesso de vtable no modelo de extensão ADSI

Uma interface dupla habilita o acesso Direct vtable a todas as suas funções, enquanto uma interface de expedição não. Um cliente C/C++ pode consultar um ponteiro de interface dupla e usar o acesso Direct vtable para invocar suas funções. Isso fornece acesso mais rápido do que chamar a função usando as funções [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) . Isso é especialmente verdadeiro no modelo de extensão, porque todas as interfaces duplas em um objeto de extensão devem delegar suas **GetIDsOfNames** e **invocar** funções de volta para o agregador (ADSI) primeiro. Em seguida, o agregador deve executar etapas internas adicionais para identificar qual objeto de extensão, possivelmente incluindo o agregador em si, fornece suporte para a função chamada e redirecionar a chamada para o objeto apropriado.

Visual Basic também invoca uma função de interface dupla usando o acesso direto a uma vtable, se ela tiver um ponteiro para a interface e o acesso ao tipo de dados da biblioteca de tipos. Os clientes ADSI escritos em Visual Basic podem especificar um ponteiro para uma interface dupla, por exemplo, [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), explicitamente e, portanto, habilitar o acesso vtable a funções na interface.


```VB
Dim inf as IADs
 
Set inf = GetObject("LDAP://CN=jeffsmith,DC=fabrikam,DC=com") ' An object that supports IADsDualInf.
inf.Get("name") 'IADs.Get() will be invoked through direct vtable access.
```



Como uma interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) não dá suporte ao acesso vtable, este exemplo não se aplica. Ou seja, uma função de expedição é sempre invocada apenas pelas funções [**IDispatch:: GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) e [**IDispatch:: Invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) .

As versões atuais do VBScript e do JScript também não dão suporte ao acesso vtable. Portanto, uma interface dupla em um ambiente VBScript ou JScript é executada como uma interface de expedição.

 

 