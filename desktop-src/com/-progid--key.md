---
title: Chave de ProgID
description: Um ProgID (identificador programático) é uma entrada de registro que pode ser associada a um CLSID. Assim como o CLSID, o ProgID identifica uma classe, mas com menos precisão porque não é garantido que seja globalmente exclusivo.
ms.assetid: f9ef2934-0815-4a6f-9283-8f748eee083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9ef64515d2dda4512af0086970cb2ab61b4830
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008734"
---
# <a name="progid-key"></a>Chave de ProgID

Um ProgID (identificador programático) é uma entrada de registro que pode ser associada a um CLSID. Assim como o CLSID, o ProgID identifica uma classe, mas com menos precisão porque não é garantido que seja globalmente exclusivo.

## <a name="registry-entry"></a>Entrada do Registro

**HKEY \_ \_Classes de \\ software \\ de computador local** \\ *{* ProgID *}*



| Chave do Registro                            | Descrição                                                        |
|-----------------------------------------|--------------------------------------------------------------------|
| [**CLSID**](clsid.md)                  | Associa um ProgID a um CLSID.                                  |
| [**Insertable**](insertable-progid.md) | Indica que essa classe é insertável em contêineres OLE 2.       |
| [**Protocolo**](protocol.md)            | Indica que esta classe OLE 2 é insertável em contêineres de OLE 1. |
| [**Shell**](shell.md)                  | Fornece informações de impressão do shell do Windows 3,1 e **abertura de arquivo** . |



 

## <a name="remarks"></a>Comentários

Você pode usar uma ProgID em situações de programação em que não é possível usar um CLSID. ProgIDs não devem aparecer na interface do usuário. Não há garantia de que os ProgIDs sejam exclusivos, portanto, eles podem ser usados apenas onde as colisões de nomes são gerenciáveis.

O formato de um ProgID é <*programa*>. <*componente*>. <*versão*>, separados por pontos e sem espaços, como em Word.Document. 6. O ProgID deve estar em conformidade com os seguintes requisitos:

-   Ter no máximo 39 caracteres.
-   Não conter nenhuma Pontuação (incluindo sublinhados), exceto um ou mais pontos.
-   Não começar com um dígito.
-   Seja diferente do nome de classe de qualquer aplicativo OLE 1, incluindo a versão de OLE 1 do mesmo aplicativo, se houver um.

Como o ProgID não deve aparecer na interface do usuário, você pode obter um nome de exibição chamando [**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype). Além disso, consulte [**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype).

A chave **HKEY \_ local \_ Machine \\ software \\ classes** corresponde à chave de **\_ \_ raiz de classes hKey** , que foi retida para compatibilidade com versões anteriores do com.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IOleObject:: GetUserType**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> <dt>

[**OleRegGetUserType**](/windows/desktop/api/Ole2/nf-ole2-olereggetusertype)
</dt> </dl>

 

 




