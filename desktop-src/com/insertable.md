---
title: Insertável (chave CLSID)
description: Indica que os objetos dessa classe devem aparecer na caixa de listagem da caixa de diálogo Inserir objeto quando usados por aplicativos de contêiner COM.
ms.assetid: 908cbfc4-ebf8-454e-b2e5-34449de60e7f
keywords:
- COM chave de registro insertável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5da4892fb13de5954dabe7c55759900dba32f854
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008754"
---
# <a name="insertable-clsid-key"></a>Insertável (chave CLSID)

Indica que os objetos dessa classe devem aparecer na caixa de listagem da caixa de diálogo **Inserir objeto** quando usados por aplicativos de contêiner com.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Insertable
```

## <a name="remarks"></a>Comentários

Essa chave é uma entrada necessária para aplicativos COM de 32 bits cujos objetos podem ser inseridos em aplicativos de 16 bits existentes. Os aplicativos de 16 bits existentes examinam o registro para essa chave, que informa ao aplicativo que o servidor oferece suporte a incorporações. Se a chave que pode ser **inserida** existir, os aplicativos de 16 bits também poderão tentar verificar se o servidor existe no computador. Normalmente, os aplicativos de 16 bits recuperam o valor da chave [**LocalServer**](localserver.md) da classe e verificam se ele é um arquivo válido no sistema. Portanto, para que um aplicativo de 32 bits seja inserido por um aplicativo de 16 bits, o aplicativo de 32 bits deve registrar a subchave **LocalServer** , além de registrar [**LocalServer32**](localserver32.md).

Usado com controles, essa entrada indica que um objeto pode agir somente como um objeto inserido in-loco sem recursos de controle especiais. Os objetos que têm essa chave aparecem na caixa de diálogo **Inserir objeto** para seu contêiner. Quando usado com controles, essa entrada também indica que o controle foi testado com contêineres que não são de controle. Essa entrada também é opcional e pode ser omitida quando um controle não é projetado para funcionar com contêineres mais antigos que não entendem controles.

> [!Note]  
> Essa chave não está presente para classes internas como as classes moniker.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**<ProgID>**](-progid--key.md)
</dt> </dl>

 

 




