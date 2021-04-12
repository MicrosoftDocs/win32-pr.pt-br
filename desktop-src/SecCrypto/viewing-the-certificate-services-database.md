---
description: A interface ICertView é usada por clientes devidamente autorizados para exibir o banco de dados de serviços de certificados.
ms.assetid: c8f316dd-186b-4e4a-b0ce-561a23b266cb
title: Exibindo o banco de dados dos serviços de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c553cee2f64c3096e733d588c9e0ad3d08ceb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091658"
---
# <a name="viewing-the-certificate-services-database"></a>Exibindo o banco de dados dos serviços de certificados

A interface [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) é usada por clientes devidamente autorizados para exibir o banco de dados de serviços de certificados. Deve-se observar que, como parte do produto enviado, o snap-in do MMC da autoridade de certificação pode ser usado para exibir o banco de dados dos serviços de certificados. O [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) é fornecido para exibir programaticamente o banco de dados. O suporte para a interface **ICertView** começa com o Windows XP.

Um cliente devidamente autorizado significa um usuário que recebeu permissão para exibir o banco de dados de serviços de certificados; o snap-in do MMC da autoridade de certificação pode ser usado para conceder ou restringir o acesso para exibir o banco de dados (em **Propriedades** para a [*autoridade de certificação*](../secgloss/c-gly.md), clique na guia **segurança** ). Além disso, para usar o objeto [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , a estação de trabalho cliente precisa ter instalado os componentes cliente dos serviços de certificados.

Embora haja vários cenários para usar o [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) e suas interfaces relacionadas, o seguinte descreve uma sequência possível para o desenvolvimento de um aplicativo cliente baseado em **ICertView**:

**Para exibir o banco de dados de serviços de certificados**

1.  Depois de obter uma instância do objeto [**ICertView**](/windows/desktop/api/Certview/nn-certview-icertview) , chame [**ICertView:: OpenConnection**](/windows/desktop/api/Certview/nf-certview-icertview-openconnection) para se comunicar com uma [*autoridade de certificação*](../secgloss/c-gly.md) em um computador específico.
2.  Chame [**ICertView:: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) para especificar o número de colunas na exibição; Essa chamada também é usada para especificar uma exibição padrão. Se uma exibição padrão não for especificada na chamada, o chamador deverá chamar [**ICertView:: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn) para cada uma das colunas a serem contidas na exibição.
3.  Opcional. Especifique critérios de classificação e/ou critérios de qualificação para a consulta de banco de dados chamando a função [**ICertView:: Restrict**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) . Os critérios de qualificação consistem em informar a exibição para recuperar dados com base em qualificadores, como maior que, menor que, igual a e assim por diante.
4.  Chame [**ICertView:: OpenView**](/windows/desktop/api/Certview/nf-certview-icertview-openview) para recuperar os dados na exibição; os dados da exibição serão compostos pelas colunas solicitadas por meio de [**ICertView:: SetResultColumnCount**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumncount) (e se uma exibição padrão não tiver sido especificada, [**ICertView:: SetResultColumn**](/windows/desktop/api/Certview/nf-certview-icertview-setresultcolumn)). Se [**ICertView:: Restrict**](/windows/desktop/api/Certview/nf-certview-icertview-setrestriction) for chamado, os dados nas colunas serão classificados e/ou qualificados. **ICertView:: OpenView** cria um objeto [**IEnumCERTVIEWROW**](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) , que pode ser usado para enumerar as linhas da exibição.
5.  Use os [](/windows/desktop/api/Certview/nn-certview-ienumcertviewrow) métodos IEnumCERTVIEWROW [**IEnumCERTVIEWROW:: EnumCertViewAttribute**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewattribute), [**IEnumCERTVIEWROW:: EnumCertViewColumn**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewcolumn)e [**IEnumCERTVIEWROW:: EnumCertViewExtension**](/windows/desktop/api/Certview/nf-certview-ienumcertviewrow-enumcertviewextension) para recuperar os dados de atributo, coluna e extensão conforme desejado.

 

 
