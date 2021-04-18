---
description: Solicita um ponto de extremidade que é usado para se conectar a um serviço.
ms.assetid: 4C02EA78-AD77-42CD-B94F-C8C3ED26CB4C
title: 'Método IUpdateEndpointProvider:: getserviceendpoint (UpdateEndpointAuth. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUpdateEndpointProvider.GetServiceEndpoint
api_type:
- COM
api_location:
- UpdateEndpointAuth.dll
ms.openlocfilehash: bddb77237d6d5edabab41eefe1931514fd6aed42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767807"
---
# <a name="iupdateendpointprovidergetserviceendpoint-method"></a>Método IUpdateEndpointProvider:: getserviceendpoint

Solicita um ponto de extremidade que é usado para se conectar a um serviço.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetServiceEndpoint(
  [in]  GUID                        ServiceId,
  [in]  UpdateEndpointType          endpointType,
  [in]  UpdateEndpointProxySettings proxySettings,
  [in]  HANDLE_PTR                  hUserToken,
  [in]  BOOL                        fRefreshOnline,
  [out] BSTR                        *pbstrEndpointLoc
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ServiceId* \[ no\]
</dt> <dd>

Identifica o serviço a ser atualizado.

</dd> <dt>

*ponto de extremidade* \[ no\]
</dt> <dd>

Identifica o tipo de ponto de extremidade implementado pelo serviço.

A enumeração [**UpdateEndpointType**](updateendpointtype.md) define as constantes a seguir.

<dt>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>

<span id="uetClientServer"></span><span id="uetclientserver"></span><span id="UETCLIENTSERVER"></span>**uetClientServer**


</dt> <dd>

Um ponto de extremidade cliente-servidor usado para se conectar ao serviço de atualização.

</dd> <dt>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>

<span id="uetReporting"></span><span id="uetreporting"></span><span id="UETREPORTING"></span>**uetReporting**


</dt> <dd>

Um ponto de extremidade de relatório usado quando o cliente relata os resultados de verificações, downloads e instalações de volta para o serviço de atualização

</dd> <dt>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>

<span id="uetWuaSelfUpdate"></span><span id="uetwuaselfupdate"></span><span id="UETWUASELFUPDATE"></span>**uetWuaSelfUpdate**


</dt> <dd>

Um ponto de extremidade Self-Update que é usado quando o computador cliente entra em contato com um serviço de atualização para ver se há uma nova versão do software cliente do Windows Update Agent.

</dd> <dt>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>

<span id="uetRegulation"></span><span id="uetregulation"></span><span id="UETREGULATION"></span>**uetRegulation**


</dt> <dd>

Um ponto de extremidade de regulamentação que é usado quando o computador cliente entra em contato com o serviço regulamento para agir em uma atualização específica aplicável ao computador de destino.

</dd> <dt>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>

<span id="uetSimpleTargeting"></span><span id="uetsimpletargeting"></span><span id="UETSIMPLETARGETING"></span>**uetSimpleTargeting**


</dt> <dd>

Um Simple-Targeting endoint que é usado somente com serviços privados (servidores WSUS em ambientes corporativos).

</dd> </dl> </dd> <dt>

*proxySettings* \[ no\]
</dt> <dd>

Identifica as configurações que são usadas ao se conectar a um servidor proxy.

</dd> <dt>

*hUserToken* \[ no\]
</dt> <dd>

Contém um objeto identificador de token que representa o usuário. O provedor de ponto de extremidade usa esse token para determinar quais configurações de proxy e credenciais usar.

</dd> <dt>

*fRefreshOnline* \[ no\]
</dt> <dd>

Indica que o WUA do clima solicita um novo token. Verdadeiro indica que um novo token é solicitado. False indica que um token novo ou armazenado em cache é solicitado. Consulte comentários para obter mais informações.

</dd> <dt>

*pbstrEndpointLoc* \[ fora\]
</dt> <dd>

Especifique a URL usada para se comunicar com o serviço. Por exemplo, para um ponto de extremidade cleint-Server, essa seria a URL para o serviço do servidor cliente. Consulte comentários para obter mais informações.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará **S \_ OK** se for bem-sucedido. Caso contrário, retorna um código de erro COM do Windows.

## <a name="remarks"></a>Comentários

O WUA normalmente define o parâmetro *fRefreshOnline* como false quando esse método é chamado pela primeira vez; em seguida, se um erro de conexão ocorrer, o WUA definirá esse parâmetro como true quando o método for chamado novamente. No entanto, a implementação desse método pode solicitar um novo token de um serviço de token de segurança (STS) ou fornecer um token em cache a qualquer momento.

Se o ponto de extremidade não precisar de autenticação, o chamador poderá se conectar ao serviço usando apenas a URL especificada pelo parâmetro *pbstrEndpointLoc* .

Se o ponto de extremidade precisar de autenticação, o chamador poderá usar a URL especificada pelo parâmetro *pbstrEndpointLoc* e os dados fornecidos pelos outros parâmetros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Somente Windows XP, Windows 2000 Professional com \[ aplicativos de área de trabalho do SP3\]<br/>                   |
| Servidor mínimo com suporte<br/> | Windows Server 2003, Windows 2000 Server com aplicativos de área de trabalho do SP3 \[ somente\]<br/>                |
| parâmetro<br/>                   | <dl> <dt>UpdateEndpointAuth. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>UpdateEndpointAuth. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>UpdateEndpointAuth. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>UpdateEndpointAuth.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IUpdateEndpointProvider**](iupdateendpointprovider.md)
</dt> </dl>

 

 




