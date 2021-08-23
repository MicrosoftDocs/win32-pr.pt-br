---
title: Compartilhamento substituto
description: Os servidores DLL compartilharão um substituto se eles têm identidades de segurança correspondentes e compartilharão o mesmo valor appid.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34e159fff59144773633cfbe35bb1486e9eeb1014d02e23e0c9b95bcd817bb53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678406"
---
# <a name="surrogate-sharing"></a>Compartilhamento substituto

Os servidores DLL compartilharão um substituto se eles têm identidades de segurança correspondentes e compartilharão o mesmo valor appid.

Os servidores DLL são carregados, por padrão, em seu próprio processo substituto. Para carregar outros servidores DLL em um substituto existente para que ele seja compatível com mais de um servidor DLL, há dois requisitos:

-   Os servidores DLL devem ter o mesmo valor appid.
-   O contexto de segurança dos servidores DLL deve ser o mesmo.

Se dois servidores DLL devem ser lançados em identidades de segurança diferentes, eles devem estar em substitutos diferentes, independentemente de suas AppIDs corresponderem.

Veja a seguir um exemplo de administração de compartilhamento substituto com AppIDs:

``` syntax
    AppID
        {12345678-0000-0000-0000-abcdabcdabcd}
            @DllSurrogate    REG_SZ
    CLSID
        {12345678-0000-0000-0000-000000000001}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp1.dll
        {12345678-0000-0000-0000-000000000002}
            @AppId    REG_SZ    {12345678-0000-0000-0000-abcdabcdabcd}
            InProcServer32
    @    REG_SZ    c:\myapp\comp2.dll
 
```

Os dois CLSIDs para componentes DLL comp1.dll e comp2.dll foram configurados para compartilhar uma AppID. A [chave AppID](appid-key.md) especifica que o servidor DLL pode ser carregado em um substituto especificando o [valor DllSurrogate.](dllsurrogate.md) Neste exemplo, o valor **DllSurrogate** é uma cadeia de caracteres vazia, indicando que a implementação do sistema padrão do substituto de DLL deve ser usada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Requisitos do servidor DLL](dll-server-requirements.md)
</dt> <dt>

[Registrando o servidor DLL para ativação substituta](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




