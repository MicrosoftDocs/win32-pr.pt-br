---
title: Implementando o objeto COM da extensão de criação de objeto
description: Uma extensão de criação de objeto é um objeto COM implementado como um servidor em processo. As extensões de criação de objeto primário e secundário devem implementar a interface IDsAdminNewObjExt.
ms.assetid: 0a8ed0ed-9dcb-4373-b549-7da3f3d9f641
ms.tgt_platform: multiple
keywords:
- Implementando o objeto COM do AD de extensão de criação de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c1a9da94caa300c1277cf6f6030357ca9d573d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104007307"
---
# <a name="implementing-the-object-creation-extension-com-object"></a>Implementando o objeto COM da extensão de criação de objeto

Uma extensão de criação de objeto é um objeto COM implementado como um servidor em processo. As extensões de criação de objeto primário e secundário devem implementar a interface [**IDsAdminNewObjExt**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjext) .

## <a name="implementing-idsadminnewobjext"></a>Implementando IDsAdminNewObjExt

Quando o assistente para criação de objetos é criado, ele inicializa cada extensão de criação de objeto chamando o método [**IDsAdminNewObjExt:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize) da extensão. O método **Initialize** fornece a extensão com informações sobre o contêiner no qual o objeto está sendo criado, o nome da classe do novo objeto e as informações sobre o próprio assistente. Se o assistente de criação de objetos for iniciado para criar um novo objeto a partir de um objeto existente, o parâmetro *pADsCopySource* não será **nulo**. Nesse caso, a extensão deve tentar obter o máximo de dados do objeto que está sendo copiado como é viável.

Depois que a extensão é inicializada, o método [**IDsAdminNewObjExt:: AddPages**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-addpages) é chamado. A extensão deve adicionar a página ou páginas ao assistente durante esse método. Uma página de assistente é criada preenchendo-se uma estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) e, em seguida, passando essa estrutura para a função [**CreatePropertySheetPage**](/windows/win32/api/prsht/nf-prsht-createpropertysheetpagea) . Em seguida, a página é adicionada ao assistente chamando a função de retorno de chamada que é passada para **AddPages** no parâmetro *lpfnAddPage* .

Antes de a página de extensão ser exibida, [**IDsAdminNewObjExt:: setObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) é chamado. Isso fornece a extensão com um ponteiro de interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) para o objeto que está sendo criado.

Enquanto a página do assistente é exibida, a página deve tratar e responder a todas as mensagens de notificação do assistente necessárias, como [**PSN \_ SetActive**](../controls/psn-setactive.md) e [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md).

Quando o usuário concluir todas as páginas do assistente, o assistente exibirá uma página "Concluir" que fornece um resumo dos dados inseridos. O assistente Obtém esses dados chamando o método [**IDsAdminNewObjExt:: GetSummaryInfo**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-getsummaryinfo) para cada uma das extensões. O método **GetSummaryInfo** fornece um **BSTR** que contém os dados de texto exibidos na página "Concluir". Uma extensão de criação de objeto não precisa fornecer dados de resumo. Nesse caso, **GetSummaryInfo** deve retornar **E \_ NOTIMPL**. **GetSummaryInfo** é chamado apenas uma vez para cada extensão, não por página, portanto, se a extensão de criação de objeto adicionar mais de uma página, a extensão deverá combinar os dados de resumo em uma cadeia de caracteres.

Quando o usuário clica no botão **concluir** na página "Concluir", o assistente chama cada um dos métodos [**IDsAdminNewObjExt:: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) da extensão com o contexto **de \_ \_ \_ preconfirmação DSA NEWOBJ CTX** . Quando isso ocorre, a extensão deve gravar os dados coletados nas propriedades apropriadas usando o método [**IADs::P UT**](/windows/desktop/api/iads/nf-iads-iads-put) ou [**IADs::P utex**](/windows/desktop/api/iads/nf-iads-iads-putex) . A interface [**IADs**](/windows/desktop/api/iads/nn-iads-iads) é fornecida para a extensão no método [**IDsAdminNewObjExt:: setObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) . A extensão não deve confirmar as propriedades armazenadas em cache chamando [**IADs:: setinfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo). Quando todas as propriedades tiverem sido gravadas, a extensão de criação do objeto primário confirmará as alterações chamando **IADs:: setinfo**. Isso é discutido em mais detalhes abaixo.

Se ocorrer um erro, a extensão será notificada sobre o erro e durante a qual operação ocorreu quando o método [**IDsAdminNewObjExt:: OnError**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-onerror) for chamado.

## <a name="implementing-a-primary-object-creation-wizard"></a>Implementando um assistente de criação de objeto primário

A implementação de um assistente de criação de objeto primário é idêntica a um assistente de criação de objeto secundário, exceto pelo fato de que um assistente de criação de objeto primário deve executar mais algumas etapas.

Antes da primeira página ser ignorada, o assistente de criação de objeto deve criar o objeto de diretório temporário. Para fazer isso, chame o método [**IDsAdminNewObjPrimarySite:: CreateNew**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-createnew) . Um ponteiro para a interface [**IDsAdminNewObjPrimarySite**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobjprimarysite) é obtido chamando [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) com **\_ IDsAdminNewObjPrimarySite IID** na interface [**IDsAdminNewObj**](/windows/desktop/api/DSAdmin/nn-dsadmin-idsadminnewobj) que é passada para [**IDsAdminNewObjExt:: Initialize**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-initialize). O método **CreateNew** cria um novo objeto temporário e chama [**IDsAdminNewObjExt:: setObject**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-setobject) para cada extensão.

Quando um assistente de criação de objeto contém mais de uma página, o sistema implementa uma página "Concluir" que exibe um resumo das informações do objeto a serem salvas. Quando o botão **concluir** na página "Concluir" for clicado, o sistema chamará cada um dos métodos [**IDsAdminNewObjExt:: WriteData**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjext-writedata) da extensão de criação de objeto e, em seguida, confirmará o objeto temporário para a memória persistente. No entanto, se o assistente de criação de objetos contiver apenas uma página, a página terá botões **OK** e **Cancelar** em vez dos botões **voltar**, **Avançar** e **Cancelar** normalmente encontrados em um assistente e nenhuma página "Concluir" será fornecida. Por isso, um assistente de extensão de criação de objeto de página única deve chamar [**IDsAdminNewObjPrimarySite:: Commit**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) para executar as operações de gravação e salvamento. Uma extensão de criação de objeto primário de página única deve chamar **Commit** em resposta à notificação [**PSN \_ WIZFINISH**](../controls/psn-wizfinish.md) .

Como outras extensões de criação de objeto podem adicionar páginas ao assistente, a extensão de criação de objeto primário pode não saber se há mais de uma página no assistente. Isso não é um problema por dois motivos: primeiro, se o sistema implementar a página "Concluir", a extensão de criação de objeto primário receberá a notificação [**PSN \_ WIZNEXT**](../controls/psn-wiznext.md) em vez da notificação **PSN \_ WIZNEXT** . Em segundo lugar, a [**confirmação**](/windows/desktop/api/DSAdmin/nf-dsadmin-idsadminnewobjprimarysite-commit) falhará de forma inofensiva se o assistente contiver mais de uma página.

 

 