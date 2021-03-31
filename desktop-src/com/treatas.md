---
title: Tratados
description: Especifica o CLSID de uma classe que pode emular a classe atual.
ms.assetid: 1d7a1677-738a-4258-9afc-e77bd0dcf40f
keywords:
- Tratar da chave do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf4340b398d6a98b0445cee932da120e23355b71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822759"
---
# <a name="treatas"></a>Tratados

Especifica o CLSID de uma classe que pode emular a classe atual.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      TreatAs = {CLSID_TreatAs}
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz do reg** .

A emulação é a capacidade de um aplicativo abrir e editar um objeto de uma classe diferente, mantendo o formato original do objeto. A resolução ocorre no computador local, portanto, no caso de ativação remota, a resolução ocorre no computador cliente usando o CLSID especificado por **tratados**.

O DCOM examina o registro local de **tratados**, mesmo se você chamar a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) e especificar um servidor remoto. Isso significa que, se você tiver uma entrada **Treats** para Class1 a ser tratada como class2 em seu computador local, mas você chamar **CoCreateInstance** para criar uma instância de Class1 e especificar um servidor remoto, o DCOM tentará criar uma instância de class2 no servidor remoto, mesmo se o class2 não estiver registrado no servidor remoto, o que fará com que a chamada de **CoCreateInstance** falhe.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Tratados autotratações**](autotreatas.md)
</dt> <dt>

[**CoGetTreatAsClass**](/windows/desktop/api/combaseapi/nf-combaseapi-cogettreatasclass)
</dt> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




