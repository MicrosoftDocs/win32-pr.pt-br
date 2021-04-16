---
description: O armazenamento protegido fornece aos aplicativos uma interface para armazenar dados de usuário que devem ser mantidos seguros ou livres da modificação.
ms.assetid: 85c1a009-c4f7-4b5a-ad96-6845a4e80de9
title: Psto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9d291b911c351cce10827b7937c6a474b7c570
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105754076"
---
# <a name="pstore"></a>Psto

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

O armazenamento protegido fornece aos aplicativos uma interface para armazenar dados de usuário que devem ser mantidos seguros ou livres da modificação.

As unidades de dados armazenadas são chamadas de itens. A estrutura e o conteúdo dos dados armazenados são opacos para o sistema de armazenamento protegido. O acesso aos itens está sujeito à confirmação de acordo com um estilo de segurança definido pelo usuário, que especifica qual confirmação é necessária para acessar os dados, como se uma senha é necessária. Além disso, o acesso a itens está sujeito a um conjunto de regras de acesso. Há uma regra de acesso para cada modo de acesso: por exemplo, leitura/gravação. Os conjuntos de regras de acesso são compostos de cláusulas de acesso. Atualmente, há suporte para dois tipos de cláusulas de acesso: Authenticode e verificação binária do chamador. Normalmente, no momento da instalação do aplicativo, um mecanismo é fornecido para permitir que um novo aplicativo solicite o acesso do usuário a itens que podem ter sido criados anteriormente por outro aplicativo.

Os itens são identificados exclusivamente pela combinação de uma chave, tipo, subtipo e nome. A chave é uma constante que especifica se o item é global para este computador ou associado somente a esse usuário. O nome é uma cadeia de caracteres, geralmente escolhida pelo usuário. O tipo e o subtipo são **GUID** s, geralmente especificados pelo aplicativo. Informações adicionais sobre tipos e subtipos são mantidas no registro do sistema e incluem atributos como nome de exibição e dicas de interface do usuário. Para subtipos, o tipo pai é fixo e incluído no registro do sistema como um atributo. Os itens do grupo de tipos são usados para uma finalidade comum: por exemplo, pagamento ou identificação. Os itens do grupo de subtipos compartilham um formato de dados comum.

## <a name="in-this-section"></a>Nesta seção

-   [**IEnumPStoreItems**](ienumpstoreitems.md)
-   [**IEnumPStoreProviders**](ienumpstoreproviders.md)
-   [**IEnumPStoreTypes**](ienumpstoretypes.md)
-   [**IPStore**](ipstore.md)
-   [**PStoreCreateInstance**](pstorecreateinstance.md)
-   [**PStoreEnumProviders**](pstoreenumproviders.md)
-   [**Constantes de Pstore**](pstore-constants.md)
-   [**Tipos de Pstore**](pstore-types.md)

 

 
