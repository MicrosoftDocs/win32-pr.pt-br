---
title: Registrando a extensão de criação de objeto
description: Quando uma DLL de extensão de criação de objeto no Active Directory Domain Services é criada, ela deve ser registrada com o registro do Windows e Active Directory Domain Services para fazer COM e os snap-ins administrativos do MMC Active Directory cientes da extensão.
ms.assetid: 6e950c6c-1a4f-4de0-9be1-004c31d4734c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27d8e2a50c2340d678fd43e546d68525afbc8a7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103917108"
---
# <a name="registering-the-object-creation-extension"></a>Registrando a extensão de criação de objeto

Quando uma DLL de extensão de criação de objeto no Active Directory Domain Services é criada, ela deve ser registrada com o registro do Windows e Active Directory Domain Services para fazer COM e os snap-ins administrativos do MMC Active Directory cientes da extensão.

## <a name="registering-in-the-windows-registry"></a>Registrando no registro do Windows

Como todos os servidores COM, uma extensão de criação de objeto deve ser registrada no registro do Windows. A extensão é registrada sob a seguinte chave:

```
HKEY_CLASSES_ROOT
   CLSID
      <extension CLSID>
         InProcServer32
            (Default) = <extension path>
            ThreadingModel = Apartment
```

" &lt; CLSID &gt; de extensão" é a representação de cadeia de caracteres do CLSID, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) . " &lt; caminho &gt; de extensão" contém o caminho e o nome de arquivo da DLL de extensão. O valor de **ThreadingModel** para todas as extensões de criação de objeto deve ser "Apartment".

## <a name="registering-with-active-directory-domain-services"></a>Registrando com Active Directory Domain Services

O registro da extensão de criação de objeto é específico de uma localidade. Se a extensão de criação de objeto se aplicar a todas as localidades, ela deverá ser registrada no objeto **displaySpecifier** da classe de objeto em todos os subcontêineres de localidade no recipiente DisplaySpecifiers. Se a extensão de criação de objeto for localizada para uma determinada localidade, registre-a no objeto **displaySpecifier** no subcontêiner dessa localidade. Para obter mais informações sobre o contêiner DisplaySpecifiers e as localidades, consulte [Exibir especificadores](display-specifiers.md) e [contêiner DisplaySpecifiers](displayspecifiers-container.md).

Há dois atributos DisplaySpecifier em que uma extensão de criação de objeto pode ser registrada. Esses são **creationWizard** e **createWizardExt**.

O atributo **creationWizard** identifica as extensões de criação de objeto primário para substituir o assistente de criação de objeto nativo ou existente em Active Directory snap-ins administrativos. Uma extensão de criação primária fornece o primeiro conjunto de páginas e é hospedada da mesma maneira que as páginas nativas. Este atributo é de valor único e requer o seguinte formato:


```C++
<CLSID>
```



O " &lt; CLSID &gt; " é a representação de cadeia de caracteres do CLSID do objeto com, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

O atributo **createWizardExt** identifica extensões de criação de objeto secundário. Uma extensão de criação secundária adiciona páginas de assistente às páginas nativas ou à extensão primária. Esse atributo tem valores múltiplos e requer o seguinte formato:


```C++
<order number>,<CLSID>
```



O " &lt; número do pedido &gt; " é um número sem sinal que representa a posição da página no assistente. Quando um assistente de criação é exibido, os valores são classificados usando uma comparação do "número de &lt; ordem" de cada valor &gt; . Se mais de um valor tiver o mesmo " &lt; número do pedido &gt; ", essas páginas serão carregadas na ordem em que são lidas do servidor de Active Directory. Se possível, você deve usar um " &lt; número de pedido" não existente &gt; (ou seja, um que não tenha sido usado por outros valores na propriedade). Não há uma posição de início prescrita e as lacunas são permitidas na &lt; sequência "número do pedido &gt; ".

O " &lt; CLSID &gt; " é a representação de cadeia de caracteres do CLSID do objeto com, conforme produzido pela função [**StringFromCLSID**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromclsid) .

 

 