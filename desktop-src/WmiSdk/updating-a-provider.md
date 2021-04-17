---
description: Às vezes, talvez seja necessário instalar uma versão mais recente de um provedor em um sistema em execução.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Atualizando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4869e6e9f7fbddc3081922f476ca021934065a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783763"
---
# <a name="updating-a-provider"></a>Atualizando um provedor

Às vezes, talvez seja necessário instalar uma versão mais recente de um provedor em um sistema em execução. Se seu provedor estiver instalado como uma DLL, você poderá instalar um novo provedor sem precisar reiniciar o serviço, reinicializar o computador ou, de outra forma, afetar os aplicativos que usam o WMI naquele momento.

O procedimento a seguir descreve como atualizar um provedor.

**Para atualizar um provedor**

1.  Crie o novo provedor.

    1.  Compile o novo provedor com um nome de DLL diferente e um **CLSID** diferente.

        Por exemplo, altere Myprov.dll para Myprov1.dll e **CLSID \_ MyProProv** para **CLSID \_ MyProv** 1.

    2.  Modifique o arquivo MOF de registro do provedor para usar o novo CLSID (CLSID \_ MyProv1), mas o mesmo nome do provedor ("MyProv").

2.  Instale o novo provedor.

    1.  Copie a nova DLL do provedor com o novo nome junto com a antiga.
    2.  Registrar automaticamente o novo provedor.

        Por exemplo, use o comando **regsvr32** **myprov1.dll** para registrar o novo provedor.

    3.  Compile o novo MOF de registro do provedor, substituindo assim o registro do provedor antigo. Até esse ponto, o antigo provedor era totalmente funcional; Agora o novo provedor está totalmente operacional.

3.  Remova a versão antiga do provedor, se necessário.

    1.  Cancele o registro da DLL antiga.

        Por exemplo, use o comando **regsvr32** **/umyprov.dll** para cancelar o registro da dll antiga.

    2.  Marque a DLL antiga a ser excluída na reinicialização chamando [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa).

Você pode usar etapas semelhantes para atualizar um provedor implementado pelo servidor local.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Configurando descritores de segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Protegendo seu provedor](securing-your-provider.md)
</dt> </dl>

 

 
