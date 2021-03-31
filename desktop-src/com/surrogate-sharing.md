---
title: Compartilhamento substituto
description: Os servidores DLL compartilharão um substituto se tiverem identidades de segurança correspondentes e compartilharem o mesmo valor AppID.
ms.assetid: 88544be1-4716-47b6-9c08-2b5b2b178e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6a934f03d42113cf73df4f059ac108801d21ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635543"
---
# <a name="surrogate-sharing"></a>Compartilhamento substituto

Os servidores DLL compartilharão um substituto se tiverem identidades de segurança correspondentes e compartilharem o mesmo valor AppID.

Os servidores DLL são carregados, por padrão, em seu próprio processo substituto. Para carregar outros servidores DLL em um substituto existente para que ele dê suporte a mais de um servidor DLL, há dois requisitos:

-   Os servidores DLL devem ter o mesmo valor AppID.
-   O contexto de segurança dos servidores DLL deve ser o mesmo.

Se dois servidores DLL forem iniciados em diferentes identidades de segurança, eles deverão estar em diferentes substitutos, se seus AppIDs corresponderem.

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

Os dois CLSIDs para componentes DLL comp1.dll e comp2.dll foram configurados para compartilhar uma AppID. A chave [AppID](appid-key.md) especifica que o servidor DLL pode ser carregado em um substituto, especificando o valor [DllSurrogate](dllsurrogate.md) . Neste exemplo, o valor de **DllSurrogate** é uma cadeia de caracteres vazia, indicando que a implementação de sistema padrão do substituto de DLL deve ser usada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Requisitos do servidor DLL](dll-server-requirements.md)
</dt> <dt>

[Registrando o servidor DLL para ativação alternativa](registering-the-dll-server-for-surrogate-activation.md)
</dt> </dl>

 

 




