---
description: A API de script para WMI contém sinalizadores, valores comuns e códigos de erro.
ms.assetid: feaab757-3167-420b-8f42-edced4cd4c53
ms.tgt_platform: multiple
title: Constantes de API de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8576d4c7ab5b6103efca4491bc00b2fcf4649ef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105796185"
---
# <a name="scripting-api-constants"></a>Constantes de API de script

O WMI usa vários tipos de constantes no parâmetro *iFlags* de chamadas de método na [API de script para o WMI](scripting-api-for-wmi.md).

Visual Basic aplicativos podem incluir a biblioteca de tipos para a API de script, Wbemdisp. tlb. Os scripts não podem acessar constantes na biblioteca de tipos, a menos que usem as <REFERENCE> <OBJECT> marcas ou do formato de arquivo XML do WSH (Windows Script Host), conforme descrito em [usando a biblioteca de tipos de script do WMI](using-the-wmi-scripting-type-library.md). Caso contrário, um script deve usar o valor da constante.

## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WbemAuthenticationLevelEnum"></span><span id="wbemauthenticationlevelenum"></span><span id="WBEMAUTHENTICATIONLEVELENUM"></span>[**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dd>

Defina os níveis de autenticação de segurança.

</dd> <dt>

<span id="WbemChangeFlagEnum"></span><span id="wbemchangeflagenum"></span><span id="WBEMCHANGEFLAGENUM"></span>[**WbemChangeFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemchangeflagenum)
</dt> <dd>

Defina como uma operação de gravação para uma classe ou uma instância é executada.

</dd> <dt>

<span id="WbemCimTypeEnum"></span><span id="wbemcimtypeenum"></span><span id="WBEMCIMTYPEENUM"></span>[**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dd>

Defina os tipos CIM válidos de um valor de propriedade.

</dd> <dt>

<span id="WbemComparisonFlagEnum"></span><span id="wbemcomparisonflagenum"></span><span id="WBEMCOMPARISONFLAGENUM"></span>[**WbemComparisonFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcomparisonflagenum)
</dt> <dd>

Defina as configurações para comparação de objeto e são usadas por [**SWbemObject. \_ CompareTo**](swbemobject-compareto-.md).

</dd> <dt>

<span id="WbemConnectOptionsEnum"></span><span id="wbemconnectoptionsenum"></span><span id="WBEMCONNECTOPTIONSENUM"></span>[**WbemConnectOptionsEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemconnectoptionsenum)
</dt> <dd>

Define um sinalizador de segurança que é usado como um parâmetro em chamadas para o método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) quando uma conexão com o WMI em um computador remoto está falhando.

</dd> <dt>

<span id="WbemErrorEnum"></span><span id="wbemerrorenum"></span><span id="WBEMERRORENUM"></span>[**WbemErrorEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum)
</dt> <dd>

Defina os erros que podem ser retornados pela [API de script para chamadas WMI](scripting-api-for-wmi.md) .

</dd> <dt>

<span id="WbemFlagEnum"></span><span id="wbemflagenum"></span><span id="WBEMFLAGENUM"></span>[**WbemFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum)
</dt> <dd>

Define constantes que são usadas por [**SWbemServices.ExecQuery**](swbemservices-execquery.md), [**SWbemServices.ExecQueryAsync**](swbemservices-execqueryasync.md), [**SWbemServices. SubclassesOf**](swbemservices-subclassesof.md)e [**SWbemServices. InstancesOf**](swbemservices-instancesof.md).

</dd> <dt>

<span id="WbemImpersonationLevelEnum"></span><span id="wbemimpersonationlevelenum"></span><span id="WBEMIMPERSONATIONLEVELENUM"></span>[**WbemImpersonationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dd>

Defina os níveis de representação de segurança. Essas constantes são usadas com [**SWbemSecurity**](swbemsecurity.md).

</dd> <dt>

<span id="WbemObjectTextFormatEnum"></span><span id="wbemobjecttextformatenum"></span><span id="WBEMOBJECTTEXTFORMATENUM"></span>[**WbemObjectTextFormatEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemobjecttextformatenum)
</dt> <dd>

Defina os formatos de texto de objeto válidos a serem usados por [**SWbemObjectEx. \_ gettext**](swbemobjectex-gettext-.md).

</dd> <dt>

<span id="WbemPrivilegeEnum"></span><span id="wbemprivilegeenum"></span><span id="WBEMPRIVILEGEENUM"></span>[**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dd>

Definir privilégios. Essas constantes são usadas com [**SWbemSecurity**](swbemsecurity.md) para conceder os privilégios necessários para algumas operações.

</dd> <dt>

<span id="WbemQueryFlagEnum"></span><span id="wbemqueryflagenum"></span><span id="WBEMQUERYFLAGENUM"></span>[**WbemQueryFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemqueryflagenum)
</dt> <dd>

Defina a profundidade da enumeração ou da consulta, que determina quantos objetos são retornados por uma chamada.

</dd> <dt>

<span id="WbemTextFlagEnum"></span><span id="wbemtextflagenum"></span><span id="WBEMTEXTFLAGENUM"></span>[**WbemTextFlagEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtextflagenum)
</dt> <dd>

Define o conteúdo do texto de objeto gerado e é usado por [**SWbemObject. \_ GetObjectText**](swbemobject-getobjecttext-.md).

</dd> <dt>

<span id="WbemTimeout"></span><span id="wbemtimeout"></span><span id="WBEMTIMEOUT"></span>[**WbemTimeout**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemtimeout)
</dt> <dd>

Define as constantes de tempo limite. Essa constante é usada por [**SWbemEventSource. NextEvent**](swbemeventsource-nextevent.md).

</dd> </dl>

## <a name="combining-flags"></a>Combinando sinalizadores

Você pode combinar sinalizadores para afetar mais de um aspecto da chamada à API.

Por exemplo, para criar uma chamada [*semisynchronous*](gloss-s.md) , o parâmetro *iFlags* em uma [**SWbemServices.Exechamada \_ CQuery**](swbemservices-execquery.md) deve conter dois sinalizadores: **WbemFlagReturnImmediately** e **WbemFlagForwardOnly**. O valor de **WbemFlagReturnImmediately** é 16 e o valor de **WbemFlagForwardOnly** é 32. Como as constantes não podem ser acessadas pelo nome, os valores desses sinalizadores são combinados, produzindo um valor *iFlags* de 48.

O exemplo de script a seguir mostra a chamada.


```VB
On Error Resume Next
For Each obj in GetObject("WinMgmts:").ExecQuery _
("SELECT * FROM Win32_NTLogEvent WHERE _ LogFile='Application'",,48)
    count  = count + 1
Next
```



Nem todos os sinalizadores podem ser combinados, pois muitos são mutuamente exclusivos e podem produzir resultados imprevisíveis.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[API de script para WMI](scripting-api-for-wmi.md)
</dt> </dl>

 

 



