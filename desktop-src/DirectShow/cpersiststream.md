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
ms.openlocfilehash: 690a0f45fab7c3612d215a859798460abc81728e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500233"
---
# <a name="cpersiststream-class"></a>Classe CPersistStream

![hierarquia de classe CPersistStream](images/pstrm01.png)

`CPersistStream` é a classe base para propriedades persistentes de filtros (ou seja, propriedades de filtro em grafos salvos).

A maneira mais simples de usar o `CPersistStream` é:

1.  Organize para o filtro para herdar esta classe.
2.  Implemente [**WriteToStream**](cpersiststream-writetostream.md) e [**ReadFromStream**](cpersiststream-readfromstream.md) em sua classe. Eles substituirão as funções aqui, que não fazem nada, mas agem como espaços reservados.
3.  Altere seu **NonDelegatingQueryInterface** para tratar de **IPersistStream**.
4.  Implemente [**SIZEMAX**](cpersiststream-sizemax.md) para retornar um limite superior no número de bytes de dados que você salvar.

    Se você salvar dados Unicode™, lembre-se de que um WCHAR é 2 bytes.

5.  Quando seus dados forem alterados, chame [**SetDirty**](cpersiststream-setdirty.md).

## <a name="version-numbers"></a>Números de versão

Em algum momento, você pode decidir alterar ou estender o formato dos seus dados. Em seguida, você desejará ter um número de versão em todos os fluxos salvos antigos para que possa dizer quando lê-los, se eles representam a forma antiga ou nova. Para ajudá-lo, essa classe grava e lê um número de versão. Quando ele é gravado, ele chama [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) para consultar a versão do software que está sendo usado no momento. (Na verdade, esse é um número de versão do layout de dados no arquivo.) Ele grava isso como a primeira coisa nos dados. Se você quiser alterar a versão, implemente (substitua) **GetSoftwareVersion**. Ele lê o número de versão do arquivo em **mPS \_ dwFileVersion** antes de chamar [**ReadFromStream**](cpersiststream-readfromstream.md), portanto, no **ReadFromStream** , você pode verificar se o **MPS \_ dwFileVersion** está lendo um arquivo de versão antiga. Normalmente, você deve aceitar arquivos cuja versão não é mais nova do que a versão do software que o está lendo.

**CPersistStream** implementa [**IPersistStream**](/windows/desktop/api/objidl/nn-objidl-ipersiststream). Para obter mais informações de implementação, consulte a referência COM no SDK da plataforma Microsoft.



| Membros de Dados Protegidos                                          | Descrição                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| \_DwFileVersion mPS                                              | Número de versão do arquivo.                                                   |
| \_FDirty mPS                                                     | Os dados para esse fluxo devem ser salvos.                                           |
| Funções de membro                                                | Descrição                                                                   |
| [**CPersistStream**](cpersiststream-cpersiststream.md)         | Constrói um objeto **CPersistStream** .                                       |
| [**Com SetDirty**](cpersiststream-setdirty.md)                     | Indica que o objeto deve ser salvo no fluxo.                        |
| Funções de membro substituíveis                                    | Descrição                                                                   |
| [**GetClassID**](cpersiststream-getclassid.md)                 | Recupera o identificador de classe deste fluxo.                                |
| [**GetSoftwareVersion**](cpersiststream-getsoftwareversion.md) | Recupera o número de versão para este formato de arquivo.                            |
| [**ReadFromStream**](cpersiststream-readfromstream.md)         | Lê os dados do filtro do fluxo.                                      |
| [**SizeMax**](cpersiststream-sizemax.md)                       | Recupera o número de bytes necessários para os dados (sem incluir o número de versão). |
| [**WriteToStream**](cpersiststream-writetostream.md)           | Grava os dados do filtro no fluxo.                                       |
| Métodos IPersistStream                                          | Descrição                                                                   |
| [**GetSizeMax**](cpersiststream-getsizemax.md)                 | Recupera o número de bytes necessários para os dados (incluindo o número de versão).     |
| [**IsDirty**](cpersiststream-isdirty.md)                       | Verifica se o objeto deve ser salvo.                                           |
| [**Carregar**](cpersiststream-load.md)                             | Carrega os dados do fluxo na memória.                                   |
| [**Salvar**](cpersiststream-save.md)                             | Salva os dados da memória no fluxo.                                     |



 

 

 
