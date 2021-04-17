---
title: Métodos de propriedade de interface
description: Muitas interfaces ADSI são projetadas para dar suporte à automação e, portanto, são interfaces duplas, pois dão suporte ao acesso de cliente por meio de interfaces IUnknown e IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Métodos de propriedade de interface
- ADSI de ADSI, referência, métodos de propriedade explicados
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105811234"
---
# <a name="interface-property-methods"></a>Métodos de propriedade de interface

Muitas interfaces ADSI são projetadas para dar suporte à automação e, portanto, são interfaces duplas, pois dão suporte ao acesso de cliente por meio de interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Clientes não de automação, como aqueles escritos em C/C++, resolvem a invocação de método diretamente, usando o método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) e chamam o método diretamente. Clientes de automação, também conhecidos como clientes com limite de nome, como aqueles escritos em Visual Basic, ou Visual Basic Scripting Edition (VBScript), devem resolver indiretamente a invocação de método usando o método [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) .

Uma interface ADSI com suporte a automação define métodos de propriedade para recuperar e modificar propriedades de um objeto que implementa a interface. Os métodos Property têm nomes que têm **Get** \_ e **Put** precedidos \_ para os nomes de propriedade apropriados, por exemplo, **Get \_ User** e **Put \_ Name**.

Cada **método \_ Get** usa um único parâmetro como saída. Esse parâmetro é um endereço alocado por método de uma variável do tipo de dados Property. No retorno, essa variável assume o valor atual da propriedade solicitada. O chamador deve liberar a memória alocada da variável quando a propriedade não for mais necessária.

Cada **método \_ Put** usa um único parâmetro como entrada para o tipo de dados da propriedade correspondente. O parâmetro contém um novo valor da propriedade.

O exemplo de código a seguir mostra a invocação dos métodos de propriedade que seguem o procedimento habitual para chamar a função de membro de um objeto.


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



O exemplo de código a seguir mostra a invocação dos métodos de propriedade em clientes de automação, que podem ser um pouco diferentes. Por exemplo, Visual Basic usa a notação de ponto.


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



Todos os parâmetros e tipos de retorno devem ser daqueles que o tipo de dados VARIANT define. Todos os métodos em uma interface dupla retornam um valor HRESULT para indicar êxito ou falha.

Para obter mais informações sobre como obter e definir propriedades em objetos ADSI, consulte [cache de propriedades](property-cache-interfaces.md).

 

 