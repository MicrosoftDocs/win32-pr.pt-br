---
description: Descreve como ler um documento XPS existente de um arquivo em um OM XPS.
ms.assetid: 92a8d19f-1c9e-4e02-a3d4-f2869ec871df
title: Ler um documento XPS em um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5c3b703de24be58db875618b575cebf9c1c0b27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297293"
---
# <a name="read-an-xps-document-into-an-xps-om"></a>Ler um documento XPS em um OM XPS

Descreve como ler um documento XPS existente de um arquivo em um OM XPS.

Para criar um OM XPS de um documento XPS, chame o método [**IXpsOMObjectFactory:: CreatePackageFromFile**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromfile) .

Antes de usar esses exemplos de código em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).

## <a name="code-example"></a>Exemplo de código

O exemplo de código a seguir pressupõe que a inicialização descrita em [inicializar um om XPS](xps-object-model-initialization.md) tenha sido bem-sucedida.


```C++
    IXpsOMPackage *package = NULL;

    hr = xpsFactory->CreatePackageFromFile(
        xpsDocumentFilename,
        FALSE,
        &package);

    // package now contains a pointer to the IXpsOMPackage
    // object that has been populated with the contents
    // of the XPS document in xpsDocumentFilename.

    // When finished with the package, release the object.
    if (NULL != package) package->Release();
```



Para criar um OM XPS de um documento XPS que é armazenado como um fluxo, chame [**IXpsOMObjectFactory:: CreatePackageFromStream**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createpackagefromstream).

## <a name="remarks"></a>Comentários

Se você escrever um OM XPS imediatamente depois de ler um pacote XPS nele, parte do conteúdo original poderá ser perdida ou alterada.

Algumas das alterações que podem ocorrer nesse caso são listadas na tabela a seguir:

| Recurso de documento                      | Ação                                                             |
|---------------------------------------|--------------------------------------------------------------------|
| Assinaturas digitais<br/>         | Removido do documento<br/>                               |
| Parte DiscardControl<br/>        | Removido do documento<br/>                               |
| Partes do documento estrangeiro<br/>     | Removido do documento<br/>                               |
| Marcação FixedPage<br/>           | Modificado a partir do original<br/>                              |
| Marcação do dicionário de recursos<br/> | Modificado a partir do original, se o sinalizador de otimização estiver definido<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Navegar no OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Gravar texto em um OM XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Desenhar gráficos em um OM XPS](draw-graphics-in-an-xps-om.md)
</dt> <dt>

[Coloque as imagens em um OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

**Usado nesta seção**
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPackage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompackage)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[Inicializar um OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[API de empacotamento](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Referência da API do documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

