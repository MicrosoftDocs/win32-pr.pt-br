---
title: Seletor de objetos de diretório
description: A caixa de diálogo Seletor de objetos de diretório permite que um usuário selecione um ou mais objetos do catálogo global, um domínio ou computador ou um grupo de trabalho.
ms.assetid: 5b3e5d71-afd2-49db-b3a2-f9a49f0b2b3a
ms.tgt_platform: multiple
keywords:
- AD do seletor de objetos de diretório
- AD do seletor de objetos
- AD de objetos, seletor de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24f6ba7fd053aa8ab3245bf72c693f0a887aa983
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007325"
---
# <a name="directory-object-picker"></a>Seletor de objetos de diretório

A caixa de diálogo Seletor de objetos de diretório permite que um usuário selecione um ou mais objetos do catálogo global, um domínio ou computador ou um grupo de trabalho. Os tipos de objeto dos quais um usuário pode selecionar incluem objetos de usuário, contato, grupo e computador. Para obter mais informações sobre Active Directory Domain Services, consulte [Active Directory Domain Services](active-directory-domain-services.md).

Para exibir uma caixa de diálogo Seletor de objetos:

1.  Chame a função [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoCreateInstanceEx**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstanceex) para criar uma instância da interface [**IDsObjectPicker**](/windows/desktop/api/Objsel/nn-objsel-idsobjectpicker) .
2.  Chame o método [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) para inicializar a caixa de diálogo.
3.  Chame o método [**IDsObjectPicker:: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog) para exibir a caixa de diálogo.
4.  Chame o método [**IDataObject:: GetData**](/windows/win32/api/objidl/nf-objidl-idataobject-getdata) da instância [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) retornada pela caixa de diálogo Seletor de objetos para recuperar os dados da [**lista de seleção do CFSTR \_ DSOP \_ DS \_ \_**](cfstr-dsop-ds-selection-list.md) . O formato da área de transferência da **lista de seleção do CFSTR \_ DSOP \_ \_ \_ DS** fornece um **HGLOBAL** que contém uma estrutura de [**\_ \_ lista de seleção do DS**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . A estrutura da **\_ \_ lista de seleção do DS** contém dados sobre os itens selecionados na caixa de diálogo Seletor de objetos.

Se o SID (identificador de segurança) for necessário para um objeto, isso deverá ser solicitado diretamente do seletor de objetos, adicionando o atributo **objectSid** à lista de atributos a serem recuperados para o objeto selecionado. Não é recomendável passar o nome do objeto retornado para a função [**LsaLookupNames**](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsalookupnames) ou [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) porque a pesquisa de nome será redundante e poderá falhar em alguns casos.

Se uma referência a todos os objetos selecionados for salva, o nome distinto não deverá ser salvo porque o objeto pode ser movido, ser renomeado ou pode ser alterado devido a diferenças de localidade. Para entidades de segurança, a **objectSid** deve ser solicitada para o objeto e salva com segurança. Se o nome da entidade de segurança for necessário posteriormente, ele poderá ser recuperado com a função [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) . Para todos os outros objetos, o **objectGUID** deve ser solicitado e salvo.

## <a name="initialization"></a>Inicialização

Quando a caixa de diálogo Seletor de objetos é inicializada, um conjunto de tipos e filtros de escopo é especificado. Os tipos de escopo especificados determinam os locais, domínios ou computadores, por exemplo, do qual um usuário pode selecionar objetos. Os filtros determinam os tipos de objetos que um usuário pode selecionar de um determinado tipo de escopo. Para obter mais informações, consulte a seção escopos e filtros abaixo.

Por padrão, um usuário pode selecionar um único objeto na caixa de diálogo Seletor de objetos de diretório. Para habilitar várias seleções, defina o sinalizador **DSOP \_ sinalizar \_ seleção** múltipla no membro **flOptions** da estrutura de [**\_ \_ informações de inicialização do DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) quando a caixa de diálogo for inicializada.

## <a name="scopes-and-filters"></a>Escopos e filtros

A lista suspensa **examinar** contém os escopos dos quais um usuário pode selecionar objetos. Um escopo é um domínio, computador, grupo de trabalho ou catálogo global que armazena dados sobre o e fornece acesso a um conjunto de objetos disponíveis. As entradas na lista escopo dependem dos tipos de escopo e do computador de destino especificado quando o método [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) foi chamado pela última vez para inicializar a caixa de diálogo Seletor de objetos.

Um tipo de escopo é uma categoria genérica de escopos, como todos os domínios da empresa aos quais o computador de destino pertence ou o catálogo global para a empresa do computador de destino ou o próprio computador de destino. Para cada tipo de escopo especificado, a caixa de diálogo usa o contexto do computador de destino para determinar as entradas da lista de escopo.

O método [**IDsObjectPicker:: Initialize**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-initialize) usa um ponteiro para uma estrutura de [**informações de \_ inicialização \_ do DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_init_info) que contém uma matriz de estruturas de [**informações de \_ \_ inicialização \_ de escopo DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) . Cada entrada na matriz **de \_ \_ \_ informações de inicialização de escopo DSOP** especifica um ou mais tipos de escopo, bem como os filtros aplicáveis e outros atributos. Os filtros determinam os tipos de objetos, como usuários, grupos, contatos e computadores, que o usuário pode selecionar em um determinado tipo de escopo. Quando o usuário seleciona um escopo na lista, a caixa de diálogo aplica os filtros para esse tipo de escopo para exibir uma lista de objetos dos quais o usuário pode selecionar.

Cada estrutura de [**\_ informações de \_ inicialização \_ de escopo DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_scope_init_info) contém uma estrutura de [**\_ \_ sinalizadores de filtro DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) que especifica os filtros para esse tipo de escopo. A estrutura de **\_ \_ sinalizadores de filtro DSOP** distingue entre os escopos de nível superior e inferior:

-   Um escopo de nível superior é um catálogo global ou um domínio que dá suporte ao [provedor LDAP](/windows/desktop/ADSI/adsi-ldap-provider)ADSI.
-   Um escopo de nível inferior inclui grupos de os e computadores individuais. A caixa de diálogo usa o provedor ADSI WinNT para acessar um escopo de nível inferior.

Há dois conjuntos de sinalizadores de filtro definidos para uso na estrutura [**de \_ \_ sinalizadores de filtro DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_filter_flags) : um para escopos de nível superior e outro para escopos de nível inferior. O membro **uplevel** da estrutura de **\_ \_ sinalizadores de filtro DSOP** é uma estrutura de [**\_ \_ \_ sinalizadores de filtro de uplevement DSOP**](/windows/desktop/api/Objsel/ns-objsel-dsop_uplevel_filter_flags) que especifica os filtros para escopos de nível superior. O membro **flDownlevel** da estrutura **de \_ \_ sinalizadores de filtro DSOP** é um conjunto de sinalizadores que especificam os filtros para escopos de nível inferior.

 

 