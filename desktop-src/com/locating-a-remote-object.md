---
title: Localizando um objeto remoto
description: Localizando um objeto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96577ddd018ab6b00c5af59a9824984c1ffe255dc91849b4391b256b493b765a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992446"
---
# <a name="locating-a-remote-object"></a>Localizando um objeto remoto

Com o advento do COM para sistemas distribuídos, o COM usa o modelo básico para criação de objeto descrito em OBJETOS de Classe COM e [CLSIDs](com-class-objects-and-clsids.md) e adiciona mais de uma maneira de localizar um objeto que pode residir em outro sistema em uma rede, sem sobrecarregar o aplicativo cliente.

O COM adicionou chaves do Registro que permitem que um servidor registre o nome do computador no qual ele reside ou o computador em que um armazenamento existente está localizado. Portanto, os aplicativos cliente precisam saber apenas a CLSID do servidor.

No entanto, para casos em que é desejado, o COM substituiu um parâmetro reservado anteriormente de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) por uma estrutura [**COSERVERINFO,**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) que permite que um cliente especifique o local de um servidor. Outro valor importante na função **CoGetClassObject** é a enumeração [**CLSCTX,**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) que especifica se o objeto esperado deve ser executado em processo, local fora do processo ou remoto fora do processo. Juntos, esses dois valores e os valores no Registro determinam como e onde o objeto deve ser executado.

> [!Note]  
> Chamadas de criação de instância, quando especificam um local de servidor, podem substituir uma configuração do Registro. O algoritmo COM usado para fazer isso é descrito na referência para a [**enumeração CLSCTX.**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)

 

A ativação remota depende da relação de segurança entre o cliente e o servidor. Para obter mais informações, consulte [Segurança em COM](security-in-com.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[CLSIDs e objetos de classe COM](com-class-objects-and-clsids.md)
</dt> <dt>

[Criando um objeto por meio de um objeto de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 