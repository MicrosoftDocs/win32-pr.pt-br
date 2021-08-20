---
description: A interface ICertView é usada por clientes autorizados corretamente para exibir o banco de dados dos Serviços de Certificados.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Exibindo o banco de dados dos Serviços de Certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e63619273ac62eb929bfbdecb23c262f59604f17966792fb5edb84c7efe9e3e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896149"
---
# <a name="viewing-the-certificate-services-database"></a>Exibindo o banco de dados dos Serviços de Certificados

A interface [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) é usada por clientes autorizados corretamente para exibir o banco de dados dos Serviços de Certificados. Deve-se lembrar que, como parte do produto enviado, o snap-in do MMC da Autoridade de Certificação pode ser usado para exibir o banco de dados dos Serviços de Certificados. [**O ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) é fornecido para exibir programaticamente o banco de dados. O suporte para a interface **ICertView** começa com Windows XP.

Um cliente autorizado corretamente significa que um usuário que recebeu permissão para exibir o banco de dados dos Serviços de Certificados; O snap-in do MMC da Autoridade de Certificação pode  ser usado para conceder ou restringir o acesso para exibir o banco de dados (em Propriedades da autoridade de certificação [*,*](../secgloss/c-gly.md)clique na **guia** Segurança). Além disso, para usar o [**objeto ICertView,**](/windows/desktop/api/Certview/nn-certview-icertview) a estação de trabalho do cliente deve ter instalado os componentes cliente dos Serviços de Certificados.

Embora haja vários cenários para usar [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) e suas interfaces relacionadas, o seguinte descreve uma possível sequência para desenvolver um aplicativo cliente com base em **ICertView**:

**Para exibir o banco de dados dos Serviços de Certificados**

1.  Depois de obter uma instância do objeto [**ICertView,**](/windows/desktop/api/Certview/nn-certview-icertview) chame [**ICertView::OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) para se comunicar com uma autoridade de [*certificação*](../secgloss/c-gly.md) em um computador específico.
2.  Chame [**ICertView::SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) para especificar o número de colunas na exibição; essa chamada também é usada para especificar uma exibição padrão. Se uma exibição padrão não for especificada na chamada, o chamador deverá chamar [**ICertView::SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) para cada uma das colunas a serem contidas na exibição.
3.  Opcional. Especifique critérios de classificação e/ou critérios de qualificação para a consulta de banco de dados chamando a [**função ICertView::SetRestriction.**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) Os critérios de qualificação consistem em informar a exibição para recuperar dados com base em qualificadores como Maior que, Menor que, Igual a e assim por diante.
4.  Chame [**ICertView::OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) para recuperar os dados na exibição; Os dados da exibição consistirão nas colunas solicitadas por meio de [**ICertView::SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (e se uma exibição padrão não tiver sido especificada, [**ICertView::SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Se [**ICertView::SetRestriction**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) tiver sido chamado, os dados nas colunas serão classificados e/ou qualificados. **ICertView::OpenView** cria um objeto [**IEnumCERTVIEWROW,**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) que pode ser usado para enumerar as linhas da exibição.
5.  Use os métodos [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) [**IEnumCERTVIEWROW::EnumCertViewAttribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**IEnumCERTVIEWROW::EnumCertViewColumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)e [**IEnumCERTVIEWROW::EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) para recuperar dados de atributo, coluna e extensão conforme desejado.

 

 
