---
description: Representa um nó em uma árvore de objetos criados como parte da análise de tinta.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Interface IContextNode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9e6ca9e65b7c14f1df3af00acece8e2ba37c85d6a2193989ab232839f1863c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713457"
---
# <a name="icontextnode-interface"></a>Interface IContextNode

Representa um nó em uma árvore de objetos criados como parte da análise de tinta.

## <a name="members"></a>Membros

A interface **IContextNode** herda da interface [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IContextNode** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IContextNode** tem esses métodos.



| Método                                                                                  | Descrição                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddContextLink**](icontextnode-addcontextlink.md)                                   | Adiciona um novo [**IContextLink**](icontextlink.md) à coleção de link de contexto do objeto **IContextNode.**<br/>                                                                                                          |
| [**Addpropertydata**](icontextnode-addpropertydata.md)                                 | Adiciona uma parte dos dados específicos do aplicativo.<br/>                                                                                                                                                                         |
| [**Confirmar**](icontextnode-confirm.md)                                                 | Modifica o tipo de confirmação, que controla o que o [**objeto IInkAnalyzer**](iinkanalyzer.md) pode alterar sobre **o IContextNode.**<br/>                                                                         |
| [**ContainsPropertyData**](icontextnode-containspropertydata.md)                       | Determina se o **objeto IContextNode** contém dados armazenados no identificador especificado.<br/>                                                                                                                |
| [**CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md) | Cria um objeto **IContextNode filho** que contém apenas informações sobre tipo, identificador e local.<br/>                                                                                                          |
| [**CreateSubNode**](icontextnode-createsubnode.md)                                     | Cria um novo objeto **IContextNode** filho.<br/>                                                                                                                                                                       |
| [**DeleteContextLink**](icontextnode-deletecontextlink.md)                             | Exclui um [**objeto IContextLink**](icontextlink.md) da coleção de links do objeto **IContextNode.**<br/>                                                                                                         |
| [**DeleteSubNode**](icontextnode-deletesubnode.md)                                     | Remove um **IContextNode filho.**<br/>                                                                                                                                                                                  |
| [**GetContextLinks**](icontextnode-getcontextlinks.md)                                 | Recupera uma coleção de [**objetos IContextLink**](icontextlink.md) que representa relações com outros **objetos IContextNode.**<br/>                                                                          |
| [**Getid**](icontextnode-getid.md)                                                     | Recupera o identificador do objeto **IContextNode.**<br/>                                                                                                                                                          |
| [**GetLocation**](icontextnode-getlocation.md)                                         | Recupera a posição e o tamanho do **objeto IContextNode.**<br/>                                                                                                                                                    |
| [**Getparentnode**](icontextnode-getparentnode.md)                                     | Recupera o nó pai deste **IContextNode na** árvore do nó de contexto.<br/>                                                                                                                                       |
| [**GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)                     | Recupera o valor que indica se um **objeto IContextNode** é parcialmente populado ou totalmente populado.<br/>                                                                                                   |
| [**Getpropertydata**](icontextnode-getpropertydata.md)                                 | Recupera dados específicos do aplicativo ou outros dados de propriedade, considerando o identificador especificado.<br/>                                                                                                                         |
| [**GetPropertyDataIds**](icontextnode-getpropertydataids.md)                           | Recupera os identificadores para os quais há dados de propriedade.<br/>                                                                                                                                                        |
| [**GetStrkeCount**](icontextnode-getstrokecount.md)                                   | Recupera o número de traços associados ao **objeto IContextNode.**<br/>                                                                                                                                       |
| [**GetStrkeId**](icontextnode-getstrokeid.md)                                         | Recupera o identificador de traço para o traço referenciado por um valor de índice dentro do **objeto IContextNode.**<br/>                                                                                                    |
| [**GetStrokeIds**](icontextnode-getstrokeids.md)                                       | Recupera uma matriz de identificadores para os traços dentro do **objeto IContextNode.**<br/>                                                                                                                              |
| [**GetRogkePacketDataById**](icontextnode-getstrokepacketdatabyid.md)                 | Recupera uma matriz que contém os dados de propriedade do pacote para o traço especificado.<br/>                                                                                                                                   |
| [**GetRogkePacketDescriptionById**](icontextnode-getstrokepacketdescriptionbyid.md)   | Recupera uma matriz que contém os identificadores de propriedade de pacote para o traço especificado.<br/>                                                                                                                            |
| [**GetSubNodes**](icontextnode-getsubnodes.md)                                         | Recupera os nós filho diretos do **objeto IContextNode.**<br/>                                                                                                                                                   |
| [**Gettype**](icontextnode-gettype.md)                                                 | Recupera o tipo do objeto **IContextNode.**<br/>                                                                                                                                                                 |
| [**GetTypeName**](icontextnode-gettypename.md)                                         | Recupera um nome de tipo acessível por humanos deste **IContextNode.**<br/>                                                                                                                                                     |
| [**IsConfirmed**](icontextnode-isconfirmed.md)                                         | Recupera um valor que indica se o **objeto IContextNode** foi confirmado. [**IInkAnalyzer não**](iinkanalyzer.md) pode alterar o tipo de nó e os traços associados para objetos **IContextNode confirmados.**<br/> |
| [**LoadPropertiesData**](icontextnode-loadpropertiesdata.md)                           | Recria os dados de propriedade internos e específicos do aplicativo para uma matriz de bytes que foi criada anteriormente com [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).<br/>                  |
| [**MoveSubNodeToPosition**](icontextnode-movesubnodetoposition.md)                     | Reordena um objeto **IContextNode** filho especificado para o índice especificado.<br/>                                                                                                                                         |
| [**RemovePropertyData**](icontextnode-removepropertydata.md)                           | Remove uma parte dos dados específicos do aplicativo.<br/>                                                                                                                                                                      |
| [**Reparent**](icontextnode-reparent.md)                                               | Move esse **objeto IContextNode** da coleção de subnódes do nó de contexto pai para a coleção de subnodos do nó de contexto especificado.<br/>                                                                         |
| [**ReparentStrkeByIdToNode**](icontextnode-reparentstrokebyidtonode.md)               | Move os dados de traço deste **IContextNode** para o **IContextNode especificado.**<br/>                                                                                                                                    |
| [**SavePropertiesData**](icontextnode-savepropertiesdata.md)                           | Recupera uma matriz de bytes que contém os dados de propriedade internos e específicos do aplicativo para este **IContextNode.**<br/>                                                                                           |
| [**Setlocation**](icontextnode-setlocation.md)                                         | Atualiza a posição e o tamanho deste **IContextNode.**<br/>                                                                                                                                                            |
| [**SetPartiallyPopulated**](icontextnode-setpartiallypopulated.md)                     | Modifica o valor que indica se esse **IContextNode** é parcial ou totalmente populado.<br/>                                                                                                                   |
| [**SetRogkes**](icontextnode-setstrokes.md)                                           | Associa os traços especificados a este **IContextNode.**<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Comentários

Os tipos de nós são descritos nas constantes Tipos de [Nó de](context-node-types.md) Contexto.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra um método que examina **um IContextNode**; O método faz o seguinte:

-   Obtém o tipo do nó de contexto. Se o nó de contexto for um nó de tinta, dica de análise ou reconhecedor personalizado não classificado, ele chamará um método auxiliar para examinar propriedades específicas do tipo de nó.
-   Se o nó tiver subnónodos, ele examinará cada subnóde chamando a si mesmo.
-   Se o nó for um nó folha de tinta, ele examinará os dados de traço do nó chamando um método auxiliar.

A API InkAnalysis permite que você crie um nó de linha que contém palavras de tinta e palavras de texto. No entanto, o analisador ignorará esses nós mistos e os tratará como nós externos. Isso terá impacto sobre a precisão da análise da detecção de anotações de tinta quando o usuário final grava nesse nó misto ou em torno dele.


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do XP Tablet PC \[ Edition\]<br/>                                                 |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                     |
| Cabeçalho<br/>                   | <dl> <dt>IACom.h (também requer IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IContextNodes**](icontextnodes.md)
</dt> <dt>

[Tipos de nó de contexto](context-node-types.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Referência de análise de tinta](ink-analysis-reference.md)
</dt> </dl>

 

