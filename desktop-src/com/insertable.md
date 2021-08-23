---
title: Inserível (chave CLSID)
description: Indica que os objetos dessa classe devem aparecer na caixa de diálogo Inserir Objeto caixa de diálogo quando usados por aplicativos de contêiner COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- CHAVE do Registro insereível COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26c2d5d781545be05821b801b9e16048d2a097927890a63ead8f602c34d95613
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678586"
---
# <a name="insertable-clsid-key"></a>Inserível (chave CLSID)

Indica que os objetos dessa classe devem aparecer na caixa de diálogo Inserir **Objeto** caixa de diálogo quando usados por aplicativos de contêiner COM.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Comentários

Essa chave é uma entrada necessária para aplicativos COM de 32 bits cujos objetos podem ser inseridos em aplicativos de 16 bits existentes. Os aplicativos de 16 bits existentes procurarão essa chave no Registro, que informa ao aplicativo que o servidor dá suporte a incorporações. Se a **chave Inserível** existir, aplicativos de 16 bits também poderão tentar verificar se o servidor existe no computador. Aplicativos de 16 bits normalmente recuperam o valor da chave [**LocalServer**](localserver.md) da classe e verificam se ele é um arquivo válido no sistema. Portanto, para que um aplicativo de 32 bits seja inserido por um aplicativo de 16 bits, o aplicativo de 32 bits deve registrar a sub-chave **LocalServer,** além de registrar [**LocalServer32**](localserver32.md).

Usada com controles, essa entrada indica que um objeto pode atuar apenas como um objeto inserido in-locar sem recursos de controle especiais. Os objetos que têm essa chave aparecem na caixa **de diálogo Inserir Objeto** para seu contêiner. Quando usada com controles, essa entrada também indica que o controle foi testado com contêineres que não são de controle. Essa entrada também é opcional e pode ser omitida quando um controle não é projetado para funcionar com contêineres mais antigos que não entendem controles.

> [!Note]  
> Essa chave não está presente para classes internas como as classes de moniker.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




