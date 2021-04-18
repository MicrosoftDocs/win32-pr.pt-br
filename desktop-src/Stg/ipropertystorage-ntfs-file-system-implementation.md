---
title: IPropertyStorage-implementação do sistema de arquivos NTFS
description: A versão 5,0 do NTFS fornece uma implementação da interface IPropertyStorage para arquivos em um volume NTFS quando os arquivos não são arquivos compostos.
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage Strctd STG, implementações, sistema de arquivos NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105749194"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>IPropertyStorage-implementação do sistema de arquivos NTFS

A versão 5,0 do NTFS fornece uma implementação da interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para arquivos em um volume NTFS quando os arquivos não são arquivos compostos.

**Para obter um ponteiro para a implementação do sistema de arquivos NTFS de IPropertySetStorage**

1.  Chame [**IPropertySetStorage:: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) usando a implementação NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).
2.  Chame [**IPropertySetStorage:: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) usando a implementação NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

## <a name="when-to-use"></a>Quando usar

Use [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) para gerenciar Propriedades em um único conjunto de propriedades. Seus métodos dão suporte à leitura, gravação e exclusão de propriedades e aos nomes de cadeia de caracteres opcionais que podem ser associados a identificadores de propriedade. Outro método permite definir os horários associados ao armazenamento de propriedades e outro permite a atribuição de um CLSID, usado para associar outro código, como o código da interface do usuário, com o conjunto de propriedades. Chamar o método [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fornece um ponteiro para a implementação NTFS de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), que permite enumerar as propriedades no conjunto.

## <a name="remarks"></a>Comentários

A implementação de NTFS fornece essencialmente os mesmos recursos que a implementação do arquivo composto. Para obter mais informações, consulte [implementação de arquivo composto IPropertyStorage](ipropertystorage-compound-file-implementation.md).

Como o NTFS é um sistema de arquivos robusto, um conjunto de propriedades NTFS nunca será deixado em um estado incorreto. Quando o conteúdo de um [**IPROPERTYSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS é liberado para o arquivo NTFS subjacente, todo ou nenhum do estado é gravado no arquivo como uma operação atômica, mesmo que haja uma falha durante a operação, como uma terminação de processo anormal. Para obter um comportamento semelhante com a implementação do arquivo composto, a interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pai deve ser aberta no modo transacionado.

Esse nível de robustez só é possível ao acessar uma propriedade NTFS definida em um volume NTFS 5,0. É possível acessar os conjuntos de propriedades NTFS em versões anteriores do NTFS (por exemplo, um computador em execução no Windows NT ou no Windows 2000 que acessa os conjuntos de propriedades em um computador do servidor de arquivos em execução no Windows NT 4,0), mas não há garantia de que eles estejam em um estado correto no caso de uma falha inesperada.

Embora a implementação NTFS do [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) não ofereça suporte à transacção, a implementação NTFS do [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dá suporte a ela. Ou seja, **STGM \_ transacionado** pode ser especificado no parâmetro *GrfMode* para os métodos [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de **IPropertySetStorage**. Como na implementação do arquivo composto, o modo transacionado é possível apenas para armazenamentos de propriedade não simples (especificando **PROPSETFLAG não \_ simples** no parâmetro *grfFlags* ).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage-implementação do sistema de arquivos NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 