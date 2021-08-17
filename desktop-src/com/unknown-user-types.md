---
title: Tipos de usuário desconhecidos
description: Tipos de usuário desconhecidos
ms.assetid: c2a4bd83-6eaf-4130-8f86-e99f1e18b63d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5ee88d36399187bab24ce51f0ef1c3c074182f98ce30ff6dc7d370992ffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129458"
---
# <a name="unknown-user-types"></a>Tipos de usuário desconhecidos

Você pode facilitar a localização do produto adicionando a seguinte chave do registro:

**HKEY \_ \_Computadores locais \\ software \\ Microsoft \\ OLE2** \\ **UnknownUserType**  =  *UserType*

Essa chave permite que o Functions retorne uma cadeia de caracteres especificada, em vez de um valor padrão de "Unknown", permitindo que os localizadores especifiquem um tipo de usuário de um idioma diferente.

A implementação do manipulador padrão COM de [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype) examina o registro chamando [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype). Se a classe do objeto não for encontrada no registro, o tipo de usuário da instância [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) do objeto será retornado. Se a classe não for encontrada na instância **IStorage** do objeto, a cadeia de caracteres "Unknown" será retornada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> </dl>

 

 