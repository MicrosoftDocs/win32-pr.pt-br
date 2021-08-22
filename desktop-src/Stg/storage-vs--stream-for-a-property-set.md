---
title: Armazenamento e objetos de fluxo para um conjunto de propriedades
description: O programador especifica se um conjunto de propriedades é armazenado em um armazenamento ou em um fluxo quando o conjunto de propriedades é criado.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e63ff148a72342da4cf5a6d8e1d59feab5c9b5b6fcbdf8a413069413cdb1e63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661835"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Armazenamento e objetos de fluxo para um conjunto de propriedades

O programador especifica se um conjunto de propriedades é armazenado em um armazenamento ou em um fluxo quando o conjunto de propriedades é criado. O \_ valor de enumeração não simples PROPSETFLAG, passado no parâmetro *grfFlags* para o método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , indica isso. Definir onde o conjunto de propriedades é armazenado fornece controles de aplicativo adequados para interoperar totalmente por meio da interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) com a propriedade com definida.

Se o \_ sinalizador não simples PROPSETFLAG for definido, o conjunto de propriedades será armazenado em um objeto de armazenamento, e os valores de propriedade não simples poderão ser gravados nele. Valores não simples incluem valores com um **VarType** de \_ armazenamento VT, transmissão de VT \_ , \_ objeto armazenado VT \_ ou \_ objeto transmitido por VT \_ . Para obter mais informações sobre valores **VarType** e como usá-los, consulte a estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Se o \_ sinalizador não simples PROPSETFLAG não for definido, somente os valores simples poderão ser gravados no conjunto de propriedades.

No objeto de armazenamento de um conjunto de propriedades não simples, um fluxo é criado com o conteúdo nomeado. Esse é o fluxo principal do conjunto de propriedades e contém todos os valores de propriedade simples. Valores de propriedade não simples (fluxos e armazenamentos) são armazenados sob o objeto de armazenamento principal do conjunto de propriedades como subfluxos e armazenamentos. Ou seja, esses valores não simples são armazenados como irmãos para o fluxo de conteúdo. O nome dos fluxos irmãos e armazenamentos é determinado pela implementação e armazenado no fluxo de conteúdo semelhante ao modo como uma propriedade de cadeia de caracteres simples é armazenada.

 

 