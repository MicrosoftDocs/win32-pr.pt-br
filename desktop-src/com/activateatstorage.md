---
title: Activateatstorage
description: Configura o cliente para insinuar objetos no mesmo computador que o estado persistente que ele está usando ou do qual eles são inicializados.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- valor do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8087313b8527ed95e7122d0e8dbe4fbd1ef028d7009f25937b3dc4300e9a4103
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048894"
---
# <a name="activateatstorage"></a>Activateatstorage

Configura o cliente para insinuar objetos no mesmo computador que o estado persistente que ele está usando ou do qual eles são inicializados.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG SZ.** Qualquer valor que comece com 'Y' ou 'y' indica que **ActivateAtStorage** deve ser usado.

A **funcionalidade ActivateAtStorage** fornece uma maneira transparente de permitir que os clientes localizem objetos em execução no mesmo computador que os dados que eles usam. Isso reduz o tráfego de rede porque o objeto executa chamadas do sistema de arquivos local em vez de chamadas pela rede.

Quando um valor é definido para **ActivateAtStorage**, esse se torna o comportamento padrão em chamadas para as funções [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage,**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) bem como para a implementação de moniker de arquivo [**de IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). Em todas essas chamadas, especificar uma estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) substitui a configuração **de ActivateAtStorage** durante a chamada de função. O chamador pode passar **informações de COSERVERINFO** para **IMoniker::BindToObject** por meio da [**estrutura BIND \_ OPTS2.**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1)

O valor definido para **ActivateAtStorage** também é o comportamento padrão quando CLSCTX REMOTE SERVER é especificado se nenhuma informação do Registro para a classe é instalada no computador do \_ \_ cliente. Os aplicativos cliente escritos para aproveitar **o ActivateAtStorage** podem, portanto, exigir menos administração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Clsctx**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**Coserverinfo**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> </dl>

 

 