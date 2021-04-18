---
description: Abre uma caixa de diálogo do sistema para solicitar permissão de usuário para dispositivos habilitados para localização.
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: Método LocationDisp. LatLongReportFactory. RequestPermissions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760695"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a>Método LocationDisp. LatLongReportFactory. RequestPermissions

\[O modelo de objeto de API de localização está disponível para uso nos sistemas operacionais especificados na seção requisitos. Ele poderá ser alterado ou ficar indisponível em versões subsequentes. Em vez disso, para acessar o local de um site, use a [API de localização geográfica do W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Para acessar o local de um aplicativo de área de trabalho, use a API [**Windows. Devices. geolocalização**](/uwp/api/Windows.Devices.Geolocation) .\]

Abre uma caixa de diálogo do sistema para solicitar permissão de usuário para dispositivos habilitados para localização.

## <a name="syntax"></a>Sintaxe


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hWnd* 
</dt> <dd>

Esse parâmetro não é usado e deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

A chamada é síncrona e o chamador aguarda a caixa de diálogo ser fechada.

> [!Note]  
> Se um aplicativo executado no modo protegido, como um BHO (objeto auxiliar de navegador) para o Internet Explorer, chamar **RequestPermissions** e o usuário escolher a opção **não habilitar este sensor de local** na caixa de diálogo, o provedor de localização não será habilitado, mas o Windows exibirá a caixa de diálogo novamente se **RequestPermissions** for chamado novamente pelo mesmo usuário. Os aplicativos executados no modo protegido podem optar por não chamar **RequestPermissions** na inicialização para que o usuário não veja uma caixa de diálogo possivelmente indesejado sempre que o aplicativo for iniciado.

 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [escutando eventos de relatório do LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/> |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                  |



 

