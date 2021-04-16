---
description: Localizando partições durante a ativação
ms.assetid: a5452ed6-ab0f-4d38-bc16-1de6cbf57486
title: Localizando partições durante a ativação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e8912c8277d79c1a20300a1a880644801d0bcb
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104571318"
---
# <a name="locating-partitions-during-activation"></a>Localizando partições durante a ativação

Localizar a partição correta na qual ativar um componente depende do seguinte:

-   A chamada de função e os parâmetros usados no programa de chamada para ativar o componente
-   Se o componente que está sendo ativado é local ou remoto
-   O uso interno do cache de partição

## <a name="the-calling-program"></a>O programa de chamada

COM+ seleciona a partição para a ativação do componente com base em como o programa de chamada ativa o componente.

Há três ações diferentes que o COM+ pode tomar ao selecionar uma partição para a ativação do componente. A ação executada depende de como o programa de chamada instancia o objeto ou seja, se a chamada de função inclui um moniker de partição, que consiste em uma ID de partição e um CLSID, ou inclui apenas um CLSID.

A tabela a seguir mostra as várias ações que o COM+ pode executar, em ordem de precedência, para localizar uma partição.



| Chamada de função                                                  | Parâmetro                                                      | Ação COM+                                                                                                                                                                                    |
|----------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) ou **GetObject**<br/> | Moniker de partição (inclui ID de partição e CLSID)<br/> | Usa a ID de partição especificada no moniker da partição.<br/>                                                                                                                           |
| [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)<br/>        | CLSID<br/>                                               | Usa a ID de partição da partição padrão da identidade do usuário ou a ID da partição que foi adicionada ao contexto durante uma ativação de componente anterior no mesmo processo.<br/> |



 

As ações COM+ listadas na tabela anterior são explicadas nas seções a seguir.

## <a name="use-of-partition-monikers"></a>Uso de monikers de partição

Uma partição pode ser selecionada explicitamente dentro de uma chamada de função usando um *moniker de partição*. Um moniker de partição é usado dentro do código para especificar explicitamente a partição do componente ativado. Se um moniker de partição for usado para localizar a partição, a ativação ocorrerá dessa partição. Ou seja, a ID da partição incluída no moniker tem precedência sobre a partição padrão do usuário ou sobre uma ID de partição que existe no contexto do chamador.

No código C++, a sintaxe para o uso de um moniker de partição é a seguinte:


```C++
HRESULT CoGetObject(
  L"partition:partitionGUID/new:clsid",
  pBindOptions,
  IID_IUnknown,
  (void**)&pIUnknown);
```



O exemplo a seguir mostra um trecho de código C++, no qual um moniker de partição está sendo usado como um argumento para a função [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) :


```C++
// Create CLSID1 configured in the Production partition.
HRESULT hr = CoGetObject(
  L"partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1",
  pBindOptions, IID_IUnknown, (void**)&pIUnknown);
```



No código Visual Basic, a sintaxe de um moniker de partição é a seguinte:


```VB
GetObject("partition:partitionGUID/new:CLSID") As Object
```



O exemplo a seguir mostra um trecho de código de Visual Basic, no qual um moniker de partição está sendo usado como um argumento para a função **GetObject** :


```VB
Dim objCLSID1 As Object
Set objCLSID1 = GetObject( _
   "partition:{35056070-D5B7-4b59-9FBF-0D23417F6937}/new:CLSID1")
```



## <a name="use-of-default-mapping"></a>Uso do mapeamento padrão

Quando a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) é usada para ativar um componente, usando o CLSID do componente, o com+ usa o mapeamento de identidade de usuário padrão, que é, o conjunto de partições ao qual o usuário está mapeado dentro Active Directory. No entanto, se o usuário não estiver mapeado para um conjunto de partições dentro do Active Directory, a partição global será selecionada.

## <a name="use-of-partition-ids-and-object-context"></a>Uso de IDs de partição e contexto de objeto

Uma das cinco propriedades atribuídas a uma nova partição é a ID da partição. Quando o programa cliente chama a função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) para criar uma instância de um objeto, a ID da partição é adicionada ao contexto. O uso da ID de partição do contexto para localizar a partição é importante porque garante que, depois que uma cadeia de ativações for iniciada, a ID da partição permanecerá a mesma, a menos que seja alterada explicitamente por meio de um moniker de partição.

Para obter informações adicionais sobre como localizar partições durante a ativação, consulte [componentes e partições em fila do com+](com--queued-components-and-partitions.md).

## <a name="local-and-remote-activation"></a>Ativação local e remota

-   Se o componente que está sendo chamado existir em outro computador, as propriedades da partição (incluindo a ID da partição) serão empacotadas para o outro computador e o componente será ativado da partição empacotada. Se nenhuma ID de partição tiver sido empacotada, COM+ usará o conjunto de partições padrão mapeado para a identidade do usuário dentro do Active Directory.

## <a name="the-partition-cache"></a>O cache de partição

Em um ambiente de domínio, o COM+ usa os mapeamentos no Active Directory para localizar a partição correta para a ativação do componente. No entanto, pesquisas frequentes no Active Directory podem resultar em excesso de tráfego de rede. Para minimizar o tráfego de rede resultante de pesquisas frequentes de mapeamento de conjunto de usuário para partição no Active Directory, o COM+ usa um *cache de partição*.

O cache de partição contém os mapeamentos que foram feitos em Active Directory entre as identidades de usuário ou as UOs e seus conjuntos de partições. Esse cache de partição está localizado no servidor de aplicativos no qual residem os aplicativos COM+.

Quando o COM+ precisa determinar a partição padrão de um usuário ou validar os direitos de acesso de um usuário para uma partição, ele verifica o cache de partição localmente para procurar o mapeamento do usuário, em vez de verificar Active Directory remotamente.

Se a pesquisa no cache da partição falhar, o COM+ verificará Active Directory. Se a pesquisa for bem-sucedida no Active Directory, o COM+ armazenará o mapeamento no cache da partição. Na próxima vez em que uma pesquisa for feita para esse mapeamento de usuário para partição, o COM+ a encontrará no cache de partição.

A ilustração a seguir mostra o processo que o COM+ usa para localizar uma partição para a ativação do componente.

![Diagrama que mostra uma árvore de solução de problemas para o processo que o COM+ usa para localizar uma partição para a ativação do componente.](images/5d00eb4e-4572-491c-85e9-33ceed2cd753.png)

O tamanho do cache e o tempo de expiração das entradas de cache são definidos por meio de chaves do registro. Para obter informações sobre como configurar essas chaves do registro, consulte [criando e configurando partições com+](creating-and-configuring-com--partitions.md).

> [!Note]  
> Se um computador servidor estiver desconectado da rede e o mapeamento de usuário para partição for alterado enquanto o servidor estiver desconectado, o cache de partição poderá conter mapeamento de usuário para partição desatualizado. Isso pode resultar em um erro de ativação se o mapeamento de usuário para partição for o mecanismo usado para ativar um componente.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Localizando um componente para ativação](locating-a-component-for-activation.md)
</dt> </dl>

 

