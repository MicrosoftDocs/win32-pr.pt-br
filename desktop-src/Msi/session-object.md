---
description: O objeto de sessão controla o processo de instalação.
ms.assetid: 013959d9-900c-45f7-b742-17b0365d6107
title: Objeto Session (Windows Installer)
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
ms.openlocfilehash: c391249d5ccc58fe9a947c9db761a77521c9776d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750595"
---
# <a name="session-object-windows-installer"></a>Objeto Session (Windows Installer)

O objeto de **sessão** controla o processo de instalação. Ele abre o banco de dados do instalador, que contém as tabelas de instalação e os dados. Esse objeto é associado a um conjunto padrão de funções de ação, cada um executando operações específicas em dados de uma ou mais tabelas. Ações personalizadas adicionais podem ser adicionadas para instalações de produtos específicas. A função de mecanismo básica é um sequenciador que busca registros sequenciais de uma tabela de sequência designada, avalia qualquer expressão de condição especificada e executa a ação designada. As ações não reconhecidas pelo mecanismo são adiadas para o objeto manipulador de interface do usuário para processamento, geralmente sequências de caixas de diálogo.

Observe que apenas um objeto de **sessão** pode ser aberto por um único processo.

## <a name="members"></a>Membros

O objeto de **sessão** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto de **sessão** tem esses métodos.



| Método                                                 | Descrição                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DoAction**](session-doaction.md)                   | Executa a ação especificada. <br/>                                                                                                                                                                                                                                |
| [**EvaluateCondition**](session-evaluatecondition.md) | Avalia uma expressão lógica que contém símbolos e valores e retorna um inteiro do msiEvaluateConditionErrorEnum de enumeração.<br/>                                                                                                                          |
| [**FeatureInfo**](session-featureinfo.md)             | Retorna um objeto [**FeatureInfo**](featureinfo-object.md) contendo informações descritivas para o recurso especificado.<br/>                                                                                                                                       |
| [**FormatRecord**](session-formatrecord.md)           | Retorna uma cadeia de caracteres formatada de dados de modelo e registro.<br/>                                                                                                                                                                                                      |
| [**Mensagem**](session-message.md)                     | Executa qualquer operação de registro em log habilitada e adia a execução para o objeto manipulador de interface do usuário associado ao mecanismo.<br/>                                                                                                                                              |
| [**Ordem**](session-sequence.md)                   | Abre uma consulta na tabela especificada, ordenando as ações pelos números na coluna sequence. Para cada linha buscada, o método [**DoAction**](session-doaction.md) é chamado, desde que qualquer expressão de condição fornecida não seja avaliada como false.<br/> |
| [**SetInstallLevel**](session-setinstalllevel.md)     | Define o nível de instalação da instalação atual para um valor especificado e recalcula os Estados Select e installed para todos os recursos.<br/>                                                                                                                    |



 

### <a name="properties"></a>Propriedades

O objeto de **sessão** tem essas propriedades.



| Propriedade                                                                  | Tipo de acesso           | Descrição                                                                                                                                                                |
|:--------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ComponentCosts**](session-componentcosts.md)<br/>               |                       | Retorna um objeto [**recordlist**](recordlist-object.md) que enumera o espaço em disco por unidade necessário para instalar um componente.<br/>                                  |
| [**ComponentCurrentState**](session-componentcurrentstate.md)<br/> |                       | Retorna o estado atual instalado do componente designado.<br/>                                                                                                |
| [**ComponentRequestState**](session-componentrequeststate.md)<br/> |                       | Obtém ou solicita uma alteração no estado de ação de uma linha na tabela de componentes.<br/>                                                                               |
| [**Backup de banco de dados**](session-database.md)<br/>                           |                       | Retorna o banco de dados para a sessão de instalação atual.<br/>                                                                                                      |
| [**FeatureCost**](session-featurecost.md)<br/>                     |                       | Retorna a quantidade total de espaço em disco (em unidades de 512 bytes) exigida pelo recurso especificado e seus recursos pai (até a raiz da tabela de recursos).<br/> |
| [**FeatureCurrentState**](session-featurecurrentstate.md)<br/>     |                       | Retorna o estado atual instalado do recurso designado.<br/>                                                                                                  |
| [**FeatureRequestState**](session-featurerequeststate.md)<br/>     | Leitura/gravação<br/> | Obtém ou solicita uma alteração no estado de seleção do registro e dos subregistros de um recurso.<br/>                                                                          |
| [**FeatureValidStates**](session-featurevalidstates.md)<br/>       |                       | Retorna um inteiro que representa os sinalizadores de bit com cada bit relevante que representa um estado de instalação válido para o recurso especificado.<br/>                             |
| [**Instalador**](session-installer.md)<br/>                         |                       | Retorna o objeto do instalador ativo.<br/>                                                                                                                            |
| [**Idioma (objeto de sessão)**](session-language.md)<br/>          |                       | Representa o identificador de idioma numérico usado pela sessão de instalação atual.<br/>                                                                            |
| [**Mode**](session-mode.md)<br/>                                   |                       | Essa propriedade é um valor que representa o sinalizador de modo designado para a sessão de instalação atual.<br/>                                                            |
| [**Produtoproperty**](session-productproperty.md)<br/>             |                       | Representa o valor da cadeia de caracteres de uma propriedade do instalador nomeada.<br/>                                                                                                      |
| [**Propriedade (objeto Session)**](session-session.md)<br/>           | Leitura/gravação<br/> | Recupera as propriedades do produto do banco de dados do produto.<br/>                                                                                                         |
| [**SourcePath**](session-sourcepath.md)<br/>                       |                       | Fornece o caminho completo para a pasta designada na imagem de mídia ou do servidor de origem.<br/>                                                                            |
| [**TargetPath**](session-targetpath.md)<br/>                       | Leitura/gravação<br/> | Fornece o caminho completo para a pasta designada na unidade de destino da instalação.<br/>                                                                               |
| [**VerifyDiskSpace**](session-verifydiskspace.md)<br/>             |                       | Retornará true se houver espaço em disco suficiente e false se o disco estiver cheio.<br/>                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista. Windows Installer no Windows Server 2003 ou no Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession é definido como 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Exemplos de script de Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




