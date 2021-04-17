---
description: A propriedade FeatureRequestState é uma propriedade de leitura/gravação do objeto de sessão.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Propriedade Session. FeatureRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1531157ab094d817d34650f8eae2ac6dc23c681c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766385"
---
# <a name="sessionfeaturerequeststate-property"></a>Propriedade Session. FeatureRequestState

A propriedade **FeatureRequestState** é uma propriedade de leitura/gravação do objeto de [**sessão**](session-object.md) . Ele pode ser usado para obter o estado de ação atual de um recurso ou para solicitar uma alteração na ação de um recurso e seus sub-recursos. O recurso deve ser nomeado na tabela de [recursos](feature-table.md) . Se uma alteração no estado de ação de um recurso for solicitada, o estado de ação de todos os componentes do recurso alterado também poderá ser alterado. O estado de ação dos componentes compartilhados por mais de um recurso será alterado conforme apropriado com base no novo estado de ação do recurso (consulte comentários). A propriedade **FeatureRequestState** também pode ser usada para configurar todos os recursos de uma vez, especificando a palavra-chave All em vez de um nome de recurso específico.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Valor da propriedade

Cadeia de caracteres necessária que especifica o nome do recurso a ser configurado. Para definir todos os recursos para um estado de solicitação desejado, use a palavra reservada não diferencia maiúsculas de minúsculas: ALL.

## <a name="remarks"></a>Comentários

O método [**SetInstallLevel**](session-setinstalllevel.md) deve ser chamado antes de chamar **FeatureRequestState**.

Se o estado atual do recurso estiver sendo solicitado, a propriedade **FeatureRequestState** retornará um dos valores a seguir.



| Nome do estado de seleção         | Significado                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown =-1  | Nenhuma ação é tomada para o recurso. Isso é equivalente a NULL.       |
| msiInstallStateAdvertised = 1 | O recurso deve ser anunciado.                                          |
| msiInstallStateAbsent = 2    | O recurso deve ser removido.                                             |
| msiInstallStateLocal = 3     | O recurso deve ser instalado como o local de execução.                              |
| msiInstallStateSource = 4    | O recurso deve ser instalado como execução de origem.                        |
| msiInstallStateDefault = 5   | O recurso deve ser reinstalado com o estado de ação atual do recurso. |



 

Por exemplo, o seguinte Obtém o estado atual de "MyFeature" de uma ação personalizada do VBScript.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Se o estado do recurso estiver sendo configurado, a propriedade **FeatureRequestState** deverá ser definida como um dos valores a seguir.



| Nome do estado de seleção          | Significado                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Anuncie o recurso.                  |
| msiInstallStateAbsent = 2     | Remova o recurso.                     |
| msiInstallStateLocal = 3      | Instale o recurso como Run-local.       |
| msiInstallStateSource = 4     | Instale o recurso como execução de origem. |



 

Por exemplo, as seguintes solicitações de uma ação personalizada do VBScript que "MyFeature" serão instaladas para serem executadas localmente no computador.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Quando **FeatureRequestState** é chamado, o instalador tenta definir o estado de ação de cada componente vinculado ao recurso especificado para o estado especificado, o melhor possível. No entanto, há situações comuns em que a solicitação não pode ser totalmente respeitada. Por exemplo, se um recurso estiver vinculado a dois componentes, componente A e componente B, por meio da tabela [FeatureComponents](featurecomponents-table.md) e o componente a tem o atributo **msidbComponentAttributesLocalOnly** e o componente b tem o atributo **msidbComponentAttributesSourceOnly** . Nesse caso, se **FeatureRequestState** for chamado com um estado solicitado de MsiInstallStateLocal ou msiInstallStateSource, a solicitação não poderá ser respeitada para ambos os componentes. Nesse caso, ambos os componentes podem ser ativados com o componente A definido como msiInstallStateLocal e o componente B definido como msiInstallStateSource.

Se mais de um recurso estiver vinculado a um único componente, o estado de ação final desse componente será determinado da seguinte maneira: se pelo menos um recurso chamar o componente a ser instalado localmente, ele será instalado msiInstallStateLocal. Se pelo menos um recurso chamar o componente a ser executado da mídia de origem, ele será instalado msiInstallStateSource. Se pelo menos um recurso chamar para a remoção do componente, o estado de ação será msiInstallStateAbsent. Para obter mais informações sobre como os recursos são selecionados para instalação, consulte a tabela de [recursos](feature-table.md) .

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o método [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Session**](session-object.md)
</dt> <dt>

[Recurso](feature-table.md)
</dt> </dl>

 

 




