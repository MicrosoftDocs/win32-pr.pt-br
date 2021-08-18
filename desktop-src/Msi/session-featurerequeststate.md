---
description: A propriedade FeatureRequestState é uma propriedade de leitura/gravação do objeto Session.
ms.assetid: ba19603b-ac81-4a8b-81ca-ad5f28974599
title: Propriedade Session.FeatureRequestState
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
ms.openlocfilehash: c1198f96dde27ec4056ad099f1bb4a3eed591fdd3d390c843cec42af82d4140e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629216"
---
# <a name="sessionfeaturerequeststate-property"></a>Propriedade Session.FeatureRequestState

A **propriedade FeatureRequestState** é uma propriedade de leitura/gravação do [**objeto Session.**](session-object.md) Ele pode ser usado para obter o estado de ação atual de um recurso ou para solicitar uma alteração na ação de um recurso e suas sub-funcionalidades. O recurso deve ser nomeado na [tabela Recurso.](feature-table.md) Se uma alteração no estado de ação de um recurso for solicitada, o estado da ação de todos os componentes do recurso alterado também poderá ser alterado. O estado de ação dos componentes compartilhados por mais de um recurso será alterado conforme apropriado com base no novo estado de ação do recurso (consulte Comentários). A **propriedade FeatureRequestState** também pode ser usada para configurar todos os recursos de uma só vez especificando a palavra-chave ALL em vez de um nome de recurso específico.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```JScript
propVal = Session.FeatureRequestState
Session.FeatureRequestState = propVal 
```



## <a name="property-value"></a>Valor da propriedade

Cadeia de caracteres necessária que especifica o nome do recurso a ser configurado. Para definir todos os recursos para um estado de solicitação desejado, use a palavra reservada que não não tem valor de maiúsculas e minúsculas: ALL.

## <a name="remarks"></a>Comentários

O [**método SetInstallLevel**](session-setinstalllevel.md) deve ser chamado antes de **chamar FeatureRequestState**.

Se o estado atual do recurso estiver sendo solicitado, a propriedade **FeatureRequestState** retornará um dos valores a seguir.



| Nome do estado de seleção         | Significado                                                               |
|------------------------------|-----------------------------------------------------------------------|
| msiInstallStateUnknown = -1  | Nenhuma ação é tomada para o recurso. Isso é equivalente a null.       |
| msiInstallStateAdvertised =1 | O recurso deve ser anunciado.                                          |
| msiInstallStateAbsent = 2    | O recurso deve ser removido.                                             |
| msiInstallStateLocal = 3     | O recurso deve ser instalado como run-local.                              |
| msiInstallStateSource = 4    | O recurso deve ser instalado como run-from-source.                        |
| msiInstallStateDefault = 5   | O recurso deve ser reinstalado com o estado de ação atual do recurso. |



 

Por exemplo, o seguinte obtém o estado atual de "MyFeature" de uma ação personalizada do VBScript.


```VB
Dim iRequestState
iRequestState = Session.FeatureRequestState("MyFeature")
```



Se o estado do recurso estiver sendo configurado, a propriedade **FeatureRequestState** deverá ser definida como um dos valores a seguir.



| Nome do estado de seleção          | Significado                                 |
|-------------------------------|-----------------------------------------|
| msiInstallStateAdvertised = 1 | Anunciar o recurso.                  |
| msiInstallStateAbsent = 2     | Remova o recurso.                     |
| msiInstallStateLocal = 3      | Instale o recurso como run-local.       |
| msiInstallStateSource = 4     | Instale o recurso como run-from-source. |



 

Por exemplo, as seguintes solicitações de uma ação personalizada do VBScript que "MyFeature" seja instalada para ser executado localmente no computador.


```VB
Session.FeatureRequestState("MyFeature")=3
```



Quando **FeatureRequestState** é chamado, o instalador tenta definir o estado de ação de cada componente vinculado ao recurso especificado para o estado especificado, o melhor possível. No entanto, há situações comuns em que a solicitação não pode ser totalmente a mesma. Por exemplo, se um recurso estiver vinculado a dois componentes, o Componente A e o Componente B, por meio da tabela [FeatureComponents](featurecomponents-table.md) e o Componente A tiver o atributo **msidbComponentAttributesLocalOnly** e o componente B tiver o atributo **msidbComponentAttributesSourceOnly.** Nesse caso, se **FeatureRequestState** for chamado com um estado solicitado de msiInstallStateLocal ou msiInstallStateSource, a solicitação não poderá ser acodada para ambos os componentes. Nesse caso, ambos os componentes podem ser ligado com o Componente A definido como msiInstallStateLocal e o Componente B definido como msiInstallStateSource.

Se mais de um recurso estiver vinculado a um único componente, o estado de ação final desse componente será determinado da seguinte maneira: se pelo menos um recurso chamar para que o componente seja instalado localmente, ele será instalado msiInstallStateLocal. Se pelo menos um recurso chamar para que o componente seja executado da mídia de origem, ele será instalado msiInstallStateSource. Se pelo menos um recurso chamar para a remoção do componente, o estado da ação será msiInstallStateAbsent. Para obter mais informações sobre como os recursos são selecionados para instalação, consulte a [Tabela de](feature-table.md) recursos.

Se a propriedade falhar, você poderá obter informações de erro estendidas usando o [**método LastErrorRecord.**](installer-lasterrorrecord.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession é definido como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sessão**](session-object.md)
</dt> <dt>

[Recurso](feature-table.md)
</dt> </dl>

 

 




