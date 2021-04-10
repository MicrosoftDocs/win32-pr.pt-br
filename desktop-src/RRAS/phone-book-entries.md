---
title: Entradas de Phone-Book
description: As entradas do catálogo telefônico contêm as informações necessárias para estabelecer uma conexão RAS. Um usuário ou administrador pode usar a caixa de diálogo rede dial-up para criar, editar e discar entradas de catálogo telefônico.
ms.assetid: 971d7020-f9fd-42d1-97c3-79ad6eba6964
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62cc01e66b5877c90b81610a5d8cf151b7cb7bd9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084790"
---
# <a name="phone-book-entries"></a>Entradas de Phone-Book

As entradas do catálogo telefônico contêm as informações necessárias para estabelecer uma conexão RAS. Um usuário ou administrador pode usar a caixa de diálogo **rede dial-up** para criar, editar e discar entradas de catálogo telefônico.

A partir do Windows NT Server 4,0, o sistema oferece suporte às funções descritas para o Windows 95, bem como várias funções adicionais que um aplicativo pode usar para trabalhar com catálogos telefônicos e entradas de catálogo telefônico.

A função [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) exibe uma folha de propriedades que permite ao usuário criar, editar ou copiar entradas de catálogo telefônico. As funções [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) e [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) chamam a função **RasEntryDlg** . Você pode usar a função [**RasRenameEntry**](/windows/desktop/api/Ras/nf-ras-rasrenameentrya) para renomear uma entrada de catálogo telefônico ou o [**RasDeleteEntry**](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya) para excluir uma entrada. O [**RasValidateEntryName**](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea) determina se uma cadeia de caracteres especificada tem o formato correto a ser usado como um nome de entrada.

Você pode usar o [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e o [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) para obter e definir informações adicionais sobre uma entrada de catálogo telefônico. Essas funções usam uma estrutura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) .

As funções [**RasGetCredentials**](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa) e [**RasSetCredentials**](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa) obtêm e definem as credenciais de usuário associadas a uma entrada de catálogo telefônico RAS especificada. Essas funções usam uma estrutura [**RASCREDENTIALS**](/previous-versions/windows/desktop/legacy/aa376730(v=vs.85)) .

A função [**RasGetCountryInfo**](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa) recupera informações de discagem específicas de país/região da lista de países de telefonia do Windows. **RasGetCountryInfo** usa a estrutura [**RASCTRYINFO**](/previous-versions/windows/desktop/legacy/aa376731(v=vs.85)) .

**Windows 95:  ** Dá suporte a um conjunto limitado de funções para trabalhar com entradas de catálogo telefônico. Você pode usar as funções [**RasCreatePhonebookEntry**](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya) e [**RasEditPhonebookEntry**](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya) para criar ou editar uma entrada de catálogo telefônico. Essas funções exibem uma caixa de diálogo na qual o usuário pode especificar informações sobre a entrada do catálogo telefônico. Você pode usar as funções [**RasGetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa) e [**RasSetEntryDialParams**](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa) para definir ou recuperar os parâmetros de conexão para uma entrada de catálogo telefônico. A função [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) recupera uma matriz de estruturas [**RASENTRYNAME**](/previous-versions/windows/desktop/legacy/aa377267(v=vs.85)) que contêm os nomes de entrada do catálogo telefônico.

 

 