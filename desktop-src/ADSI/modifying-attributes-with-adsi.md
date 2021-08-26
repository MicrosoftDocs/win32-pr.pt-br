---
title: Modificando atributos com ADSI
description: Para modificar valores de atributo, a ADSI fornece os métodos IADs. put e IADs. PutEx. Esses métodos modificam os dados no cache do lado do cliente. O método IADs. setinfo deve ser chamado para confirmar as alterações no diretório.
ms.assetid: cbb5c313-3b9d-4943-bd16-6e4489abe804
ms.tgt_platform: multiple
keywords:
- Modificando atributos com ADSI
- Atributos ADSI, modificando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef82d6a3d4c486fcd1fca1f5cba7ae62f57e66e713ed84551a5a9372cdc86683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079956"
---
# <a name="modifying-attributes-with-adsi"></a>Modificando atributos com ADSI

Para modificar valores de atributo, a ADSI fornece os métodos [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) e [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) . Esses métodos modificam os dados no cache do lado do cliente. O método [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) deve ser chamado para confirmar as alterações no diretório.

> [!Note]  
> Quando várias alterações de atributo são confirmadas em uma única chamada para [**IADs. setinfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo), se qualquer atributo único não puder ser modificado, nenhum dos atributos será modificado. Por exemplo, se você modificar os atributos [**SN**](/windows/desktop/ADSchema/a-sn) e [**excertoname**](/windows/desktop/ADSchema/a-givenname) e limpar o atributo [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber) de um objeto de usuário sem nenhuma chamada subsequente para o método **setinfo** , as alterações serão inseridas quando você chamar **setinfo**. Se uma ou mais das modificações não forem permitidas e, portanto, não puderem ser executadas, nenhuma das modificações coletiva feitas nos atributos será inserida durante a chamada para **setinfo**.

 

O método [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put) usa um nome de atributo e um parâmetro VARIANT. Use este método para definir atributos que contêm valores únicos e múltiplos.

O método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) fornece controle sobre as operações em atributos com valores múltiplos. Você pode acrescentar, excluir, atualizar e limpar os valores existentes. O método **IADs. PutEx** sempre espera uma matriz variante de valores de atributo. No entanto, você pode usar esse método para definir um atributo com um único valor também.

O método [**IADs. PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) usa as operações especificadas pela enumeração [**\_ enum da \_ operação \_ de propriedade ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) .

 

 