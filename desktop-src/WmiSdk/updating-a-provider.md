---
description: Às vezes, talvez seja necessário instalar uma versão mais recente de um provedor em um sistema em execução.
ms.assetid: 44c4c16a-fd79-483a-81ef-a0f74a2cdf45
ms.tgt_platform: multiple
title: Atualizando um provedor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8c40a3d50672115478ae62135774f5a1aad93373bd5b844402e89462b44fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757646"
---
# <a name="updating-a-provider"></a>Atualizando um provedor

Às vezes, talvez seja necessário instalar uma versão mais recente de um provedor em um sistema em execução. Se o provedor estiver instalado como uma DLL, você poderá instalar um novo provedor sem precisar reiniciar o serviço, reinicializar o computador ou, de outra forma, afetar todos os aplicativos que usam o WMI nesse momento.

O procedimento a seguir descreve como atualizar um provedor.

**Para atualizar um provedor**

1.  Crie o novo provedor.

    1.  Compile o novo provedor com um nome de DLL diferente e um **CLSID diferente.**

        Por exemplo, altere Myprov.dll para Myprov1.dll e **CLSID \_ MyProProv para** **CLSID \_ MyProv** 1.

    2.  Modifique o arquivo MOF de registro do provedor para usar o novo CLSID (CLSID MyProv1), mas o mesmo nome \_ de provedor ("MyProv").

2.  Instale o novo provedor.

    1.  Copie a nova DLL do provedor com o novo nome junto com o antigo.
    2.  Registre o novo provedor por conta própria.

        Por exemplo, use o **comando regsvr32** **myprov1.dll** para registrar o novo provedor.

    3.  Compile o novo MOF de registro de provedor, assim, sobrescrever o registro do provedor antigo. Até esse ponto, o provedor antigo era totalmente funcional; agora o novo provedor está totalmente operacional.

3.  Remova a versão antiga do provedor, se necessário.

    1.  Não registro da DLL antiga.

        Por exemplo, use o **comando regsvr32** **/umyprov.dll** para não fazer o registro da DLL antiga.

    2.  Marque a DLL antiga a ser excluída na reinicialização chamando [**MoveFileEx.**](/windows/desktop/api/winbase/nf-winbase-movefileexa)

Você pode seguir etapas semelhantes para atualizar um provedor local implementado pelo servidor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo um provedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Definindo Descritores de Segurança namepace](setting-namespace-security-descriptors.md)
</dt> <dt>

[Proteger seu provedor](securing-your-provider.md)
</dt> </dl>

 

 
