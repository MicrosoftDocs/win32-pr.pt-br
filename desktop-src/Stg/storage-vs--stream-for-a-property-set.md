---
title: Objetos de armazenamento e de fluxo para um conjunto de propriedades
description: O programador especifica se um conjunto de propriedades é armazenado em um armazenamento ou em um fluxo quando o conjunto de propriedades é criado.
ms.assetid: d0ca649a-d405-4c34-af02-9c2ca8b2790e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4ebd5d03c3b17e02aa47a7a859576b4cc04607a
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104008521"
---
# <a name="storage-and-stream-objects-for-a-property-set"></a>Objetos de armazenamento e de fluxo para um conjunto de propriedades

O programador especifica se um conjunto de propriedades é armazenado em um armazenamento ou em um fluxo quando o conjunto de propriedades é criado. O \_ valor de enumeração não simples PROPSETFLAG, passado no parâmetro *grfFlags* para o método [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) , indica isso. Definir onde o conjunto de propriedades é armazenado fornece controles de aplicativo adequados para interoperar totalmente por meio da interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) com a propriedade com definida.

Se o \_ sinalizador não simples PROPSETFLAG for definido, o conjunto de propriedades será armazenado em um objeto de armazenamento, e os valores de propriedade não simples poderão ser gravados nele. Valores não simples incluem valores com um **VarType** de \_ armazenamento VT, transmissão de VT \_ , \_ objeto armazenado VT \_ ou \_ objeto transmitido por VT \_ . Para obter mais informações sobre valores **VarType** e como usá-los, consulte a estrutura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Se o \_ sinalizador não simples PROPSETFLAG não for definido, somente os valores simples poderão ser gravados no conjunto de propriedades.

No objeto de armazenamento de um conjunto de propriedades não simples, um fluxo é criado com o conteúdo nomeado. Esse é o fluxo principal do conjunto de propriedades e contém todos os valores de propriedade simples. Valores de propriedade não simples (fluxos e armazenamentos) são armazenados sob o objeto de armazenamento principal do conjunto de propriedades como subfluxos e armazenamentos. Ou seja, esses valores não simples são armazenados como irmãos para o fluxo de conteúdo. O nome dos fluxos irmãos e armazenamentos é determinado pela implementação e armazenado no fluxo de conteúdo semelhante ao modo como uma propriedade de cadeia de caracteres simples é armazenada.

 

 