---
description: Os terminais conectáveis são classificados em superclasses de terminal.
ms.assetid: 0ab2896e-3634-47f7-b1f4-e7d1ffcb3592
title: Entradas do registro (API de telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afd6e4e4d91b65e3ef886fd4d2d44b571f4ac4696697aef8b8d8b2715e273e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117761163"
---
# <a name="registry-entries-telephony-api"></a>Entradas do registro (API de telefonia)

Os terminais conectáveis são classificados em superclasses de terminal. Cada superclasse de terminal tem uma entrada no registro sob a seguinte chave:

**HKEY \_ \_computador LOCAL** \\ **SOFTWARE** de \\ **telefonia Microsoft** \\ **Windows** \\ **CurrentVersion** \\  \\ **terminalmanager**

Abaixo da chave de superclasse de terminal estão entradas para cada terminal conectável na superclasse do terminal.

A entrada para cada superclasse de terminal é identificada por um CLSID de superclasse de terminal. Este é um identificador exclusivo para uma classe de terminal. A classe terminal tem um atributo opcional: Name, que é um nome amigável para a classe terminal. Cada terminal conectável é identificado por uma classe de terminal de CLSID; ou seja, um GUID. Os atributos para terminal conectável são armazenados em valores de chave de terminal conectáveis. Os atributos para um terminal conectável são os seguintes.



| Classe terminal | Nome da chave | Identificador público                                                                 |
|----------------|----------|-----------------------------------------------------------------------------------|
| Nome           | REG \_ sz  | Nome amigável do terminal                                                            |
| Empresa        | REG \_ sz  | Nome da empresa                                                                      |
| Versão        | REG \_ sz  | Informações da versão                                                               |
| CLSID          | REG \_ sz  | CLSID de terminal (usado no método COM [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ) |
| Instruções     | DWORD    | Direção do terminal                                                                |
| MediaTypes     | DWORD    | Tipos de mídia de terminal com suporte                                                    |



 

Para uma classe terminal, os atributos são os seguintes.



| CLSID | Nome da chave | Identificador público            |
|-------|----------|------------------------------|
| Nome  | REG \_ sz  | Nome amigável da classe de terminal |



 

 

 
