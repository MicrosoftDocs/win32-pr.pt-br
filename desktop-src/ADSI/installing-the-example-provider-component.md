---
title: Instalando o componente de provedor de exemplo
description: Depois de instalar o SDK do ADSI, no diretório de instalação, altere os diretórios para o \\ subdiretório Samples NetDs \\ ADSI \\ Samples do \\ provedor de \\ instalação. Execute Install.bat conforme descrito no arquivo README.TXT.
ms.assetid: 7bf4bf22-38ac-4b0d-946e-5f60c7693707
ms.tgt_platform: multiple
keywords:
- Instalando o componente do provedor de exemplo ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92e58fb471385b862982904e69a432bec1a94e3b9aff0248fdacd9f5e9c7a3e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333236"
---
# <a name="installing-the-example-provider-component"></a>Instalando o componente de provedor de exemplo

Depois de instalar o SDK do ADSI, no diretório de instalação, altere os diretórios para o \\ subdiretório Samples NetDs \\ ADSI \\ Samples do \\ provedor de \\ instalação. Execute Install.bat conforme descrito no arquivo README.TXT.

O provedor ADSI de exemplo adicionará as seguintes subchaves e valores ao registro quando Install.bat arquivo for executado:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               Sample = SampleNamespace
```

```
HKEY_CLASSES_ROOT
   SampleNamespace
      Clsid = {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   Sample
      Clsid = {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D0-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Namespace Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = SampleNamespace
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

```
HKEY_CLASSES_ROOT
   CLSID
      {F46430D1-CBfB-11CE-A9F7-00AA00B67689}
         (Default) = Sample Provider Object
         InprocServer32
            (Default) = adssmp.dll
            ThreadingModel = Both
         ProgID
            (Default) = Sample
         TypeLib
            (Default) = {F46430D2-CBfB-11CE-A9F7-00AA00B67689}
         Version
            (Default) = 0.0
```

Existem outras entradas de registro para o componente de provedor de exemplo porque o componente de provedor de exemplo implementou sua hierarquia de diretório no registro. Isso, de forma alguma, implica que outros provedores desejam ou devem fazer o mesmo.

 

 




