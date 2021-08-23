---
description: O objeto Session controla o processo de instalação.
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: Objeto Session (Windows Instalador)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7b02d1f617f7e558acd9c0423dd785c84e0175f195ee0085b2fdc79d66054683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628916"
---
# <a name="session-object-windows-installer"></a>Objeto Session (Windows Instalador)

O **objeto Session** controla o processo de instalação. Ele abre o banco de dados do Instalador, que contém as tabelas de instalação e os dados. Esse objeto está associado a um conjunto padrão de funções de ação, cada uma executando operações específicas em dados de uma ou mais tabelas. Ações personalizadas adicionais podem ser adicionadas para instalações de produtos específicas. A função básica do mecanismo é um sequenciador que busca registros sequenciais de uma tabela de sequência designada, avalia qualquer expressão de condição especificada e executa a ação designada. As ações não reconhecidas pelo mecanismo são adiadas para o objeto do manipulador de interface do usuário para processamento, geralmente sequências de caixa de diálogo.

Observe que apenas um **objeto Session** pode ser aberto por um único processo.

## <a name="members"></a>Membros

O **objeto Session** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto Session** tem esses métodos.



| Método                                                 | Descrição                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Doaction**](session-doaction.md)                   | Executa a ação especificada. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Avalia uma expressão lógica que contém símbolos e valores e retorna um inteiro da enumeração msiEvaluateConditionErrorEnum.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Retorna um [**objeto FeatureInfo**](featureinfo-object.md) que contém informações descritivas para o recurso especificado.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Retorna uma cadeia de caracteres formatada de dados de modelo e registro.<br/>                                                                                                                                                                                                      |
| [**Mensagem**](session-message.md)                     | Executa qualquer operação de registro em log habilitada e adia a execução para o objeto do manipulador de interface do usuário associado ao mecanismo.<br/>                                                                                                                                              |
| [**Sequência**](session-sequence.md)                   | Abre uma consulta na tabela especificada, ordenando as ações pelos números na coluna Sequência. Para cada linha buscada, o [**método DoAction**](session-doaction.md) é chamado, desde que qualquer expressão de condição fornecida não seja avaliada como False.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Define o nível de instalação para a instalação atual como um valor especificado e recalcula os estados Selecionar e Instalado para todos os recursos.<br/>                                                                                                                    |



 

### <a name="properties"></a>Propriedades

O **objeto Session** tem essas propriedades.



| Propriedade                                                                  | Tipo de acesso           | Descrição                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Retorna um [**objeto RecordList**](recordlist-object.md) enumerando o espaço em disco por unidade necessário para instalar um componente.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Retorna o estado instalado atual do componente designado.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Obtém ou solicita uma alteração no estado Ação de uma linha na tabela Componente.<br/>                                                                               |
| [**Banco de dados**](session-database.md)<br/>                           |                       | Retorna o banco de dados para a sessão de instalação atual.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Retorna a quantidade total de espaço em disco (em unidades de 512 bytes) exigida pelo recurso especificado e seus recursos pai (até a raiz da tabela Recurso).<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Retorna o estado instalado atual do recurso designado.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Leitura/gravação<br/> | Obtém ou solicita uma alteração no estado Selecionar do registro e dos sub-registros de um recurso.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Retorna um inteiro que representa sinalizadores de bit com cada bit relevante que representa um estado de instalação válido para o recurso especificado.<br/>                             |
| [**Instalador**](session-installer.md)<br/>                         |                       | Retorna o objeto do instalador ativo.<br/>                                                                                                                            |
| [**Idioma (Objeto de Sessão)**](session-language.md)<br/>          |                       | Representa o identificador de idioma numérico usado pela sessão de instalação atual.<br/>                                                                            |
| [**Modo**](session-mode.md)<br/>                                   |                       | Essa propriedade é um valor que representa o sinalizador de modo designado para a sessão de instalação atual.<br/>                                                            |
| [**ProductProperty**](session-productproperty.md)<br/>             |                       | Representa o valor da cadeia de caracteres de uma propriedade do instalador nomeado.<br/>                                                                                                      |
| [**Propriedade (Objeto de Sessão)**](session-session.md)<br/>           | Leitura/gravação<br/> | Recupera as propriedades do produto do banco de dados do produto.<br/>                                                                                                         |
| [**Sourcepath**](session-sourcepath.md)<br/>                       |                       | Fornece o caminho completo para a pasta designada na mídia de origem ou na imagem do servidor.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Leitura/gravação<br/> | Fornece o caminho completo para a pasta designada na unidade de destino de instalação.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Retornará true se houver espaço em disco suficiente e false se o disco estiver cheio.<br/>                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Instalador 5.0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Instalador 4.0 ou Windows Instalador 4.5 no Windows Server 2008 ou Windows Vista. Windows Instalador no Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISession é definido como \_ 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Exemplos de script do instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




