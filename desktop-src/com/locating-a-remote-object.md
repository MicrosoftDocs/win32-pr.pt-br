---
title: Localizando um objeto remoto
description: Localizando um objeto remoto
ms.assetid: b329de53-646b-42a2-afa3-06473c3483d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d0ce1b2280faaed7be3b5afb25a48438ff1a2b7
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103824024"
---
# <a name="locating-a-remote-object"></a>Localizando um objeto remoto

Com o advento do COM para sistemas distribuídos, o COM usa o modelo básico para a criação de objetos descritos em [objetos de classe com e CLSIDs](com-class-objects-and-clsids.md) e adiciona mais de uma maneira de localizar um objeto que pode residir em outro sistema em uma rede, sem sobrecarregar o aplicativo cliente.

COM adicionou chaves do registro que permitem que um servidor Registre o nome do computador no qual ele reside ou o computador onde um armazenamento existente está localizado. Portanto, os aplicativos cliente precisam saber apenas o CLSID do servidor.

No entanto, para casos em que é desejado, o COM substituiu um parâmetro anteriormente reservado de [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) por uma estrutura [**COSERVERINFO**](/windows/win32/api/objidlbase/ns-objidlbase-coserverinfo) , que permite que um cliente especifique o local de um servidor. Outro valor importante na função **CoGetClassObject** é a enumeração [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) , que especifica se o objeto esperado deve ser executado no processo, fora do processo local ou remoto fora do processo de execução. Juntos, esses dois valores e os valores no registro determinam como e onde o objeto deve ser executado.

> [!Note]  
> As chamadas de criação de instância, quando especificam um local do servidor, podem substituir uma configuração do registro. O algoritmo COM usado para fazer isso é descrito na referência para a enumeração [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) .

 

A ativação remota depende da relação de segurança entre o cliente e o servidor. Para obter mais informações, consulte [segurança em com](security-in-com.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos de classe COM e CLSIDs](com-class-objects-and-clsids.md)
</dt> <dt>

[Criando um objeto por meio de um objeto de classe](creating-an-object-through-a-class-object.md)
</dt> </dl>

 

 