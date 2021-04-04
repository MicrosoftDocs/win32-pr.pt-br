---
title: ActivateAtStorage
description: Configura o cliente para instanciar objetos no mesmo computador que o estado persistente que estão usando ou dos quais eles são inicializados.
ms.assetid: bc0f0c1c-dbfc-4b7a-b897-3646afe3f6bb
keywords:
- COM valor do registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2ddd1330191d7b7baf37973dbfb40e267a2f87e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104008454"
---
# <a name="activateatstorage"></a>ActivateAtStorage

Configura o cliente para instanciar objetos no mesmo computador que o estado persistente que estão usando ou dos quais eles são inicializados.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      ActivateAtStorage = value
```

## <a name="remarks"></a>Comentários

Este é um valor de **\_ sz do reg** . Qualquer valor que comece com "Y" ou "y" indica que **ActivateAtStorage** deve ser usado.

O recurso **ActivateAtStorage** fornece uma maneira transparente de permitir que os clientes localizem objetos em execução no mesmo computador que os dados que eles usam. Isso reduz o tráfego de rede porque o objeto executa chamadas de sistema de arquivos locais em vez de chamadas pela rede.

Quando um valor é definido para **ActivateAtStorage**, isso se torna o comportamento padrão em chamadas para as funções [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile) e [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage) , bem como para a implementação do moniker do arquivo de [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject). Em todas essas chamadas, especificar uma estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) substitui a configuração de **ActivateAtStorage** pela duração da chamada de função. O chamador pode passar informações de **COSERVERINFO** para **IMoniker:: BindToObject** por meio da estrutura [**BIND \_ OPTS2**](/windows/win32/api/objidl/ns-objidl-bind_opts2~r1) .

O valor definido para **ActivateAtStorage** também será o comportamento padrão quando o \_ servidor remoto CLSCTX \_ for especificado se nenhuma informação de registro para a classe estiver instalada no computador do cliente. Os aplicativos cliente escritos para tirar proveito do **ActivateAtStorage** podem, portanto, exigir menos administração.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> <dt>

[**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
</dt> <dt>

[**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
</dt> <dt>

[**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo)
</dt> <dt>

[**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)
</dt> <dt>

[Registrando servidores COM](registering-com-servers.md)
</dt> </dl>

 

 