---
description: CPersistStream é a classe base para propriedades persistentes de filtros (ou seja, propriedades de filtro em grafos salvos).
ms.assetid: 8073e2be-aaf9-4b01-a7d5-bab5c1dcc19b
title: Classe CPersistStream
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60a48b35ae1559e9b8dfa718c5bca38689cdf0101ce4a343a907b713c8988de0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073571"
---
# <a name="cpersiststream-class"></a>Classe CPersistStream

![Hierarquia de classes cpersiststream](images/pstrm01.png)

`CPersistStream` é a classe base para propriedades persistentes de filtros (ou seja, propriedades de filtro em grafos salvos).

A maneira mais simples de usar `CPersistStream` é:

1.  Organize o filtro para herdar essa classe.
2.  Implemente [**WriteToStream**](cpersiststream-writetostream.md) [**e ReadFromStream**](cpersiststream-readfromstream.md) em sua classe. Elas substituirão as funções aqui, que não fazem nada além de atuar como espaço reservados.
3.  Altere **o NonDeltingQueryInterface** para manipular **IPersistStream.**
4.  Implemente [**SizeMax**](cpersiststream-sizemax.md) para retornar um limite superior no número de bytes de dados que você salvar.

    Se você salvar dados Unicode™, lembre-se de que um WCHAR é de 2 bytes.

5.  Quando os dados mudarem, chame [**SetDirty**](cpersiststream-setdirty.md).

## <a name="version-numbers"></a>Números de versão

Em algum momento, você pode decidir alterar ou estender o formato dos seus dados. Em seguida, você desejará ter um número de versão em todos os fluxos salvos antigos para poder saber, ao lê-los, se eles representam o formulário antigo ou novo. Para ajudá-lo, essa classe grava e lê um número de versão. Quando ele grava, ele chama [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) para perguntar sobre a versão do software que está sendo usado no momento. (Na verdade, esse é um número de versão do layout de dados no arquivo.) Ele grava isso como a primeira coisa nos dados. Se você quiser alterar a versão, implemente (substitua) **GetSoftwareVersion.** Ele lê o número de versão do arquivo no **mPS \_ dwFileVersion** antes de chamar [**ReadFromStream,**](cpersiststream-readfromstream.md)portanto, em **ReadFromStream,** você pode verificar **mPS \_ dwFileVersion** para ver se você está lendo um arquivo de versão antigo. Normalmente, você deve aceitar arquivos cuja versão não é mais recente do que a versão de software que os está lendo.

**O CPersistStream** implementa [**IPersistStream.**](/windows/desktop/api/objidl/nn-objidl-ipersiststream) Para obter mais informações de implementação, consulte a Referência COM no SDK da Microsoft Platform.



| Membros de Dados Protegidos                                          | Descrição                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| mPS \_ dwFileVersion                                              | Número de versão do arquivo.                                                   |
| mPS \_ fDirty                                                     | Os dados desse fluxo devem ser salvos.                                           |
| Funções de membro                                                | Descrição                                                                   |
| [**Cpersiststream**](cpersiststream-cpersiststream.md)         | Constrói **um objeto CPersistStream.**                                       |
| [**Setdirty**](cpersiststream-setdirty.md)                     | Indica que o objeto deve ser salvo no fluxo.                        |
| Funções de membro que podem ser substituídos                                    | Descrição                                                                   |
| [**Getclassid**](cpersiststream-getclassid.md)                 | Recupera o identificador de classe desse fluxo.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Recupera o número de versão para esse formato de arquivo.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Lê os dados do filtro do fluxo.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Recupera o número de bytes necessários para os dados (não incluindo o número de versão). |
| [**Writetostream**](cpersiststream-writetostream.md)           | Grava os dados do filtro no fluxo.                                       |
| Métodos IPersistStream                                          | Descrição                                                                   |
| [**Getsizemax**](cpersiststream-getsizemax.md)                 | Recupera o número de bytes necessários para os dados (incluindo o número de versão).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Verifica se o objeto deve ser salvo.                                           |
| [**Carregar**](cpersiststream-load.md)                             | Carrega os dados do fluxo na memória.                                   |
| [**Salvar**](cpersiststream-save.md)                             | Salva os dados da memória no fluxo.                                     |



 

 

 
