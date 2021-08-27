---
title: Interface IMsRdpClientAdvancedSettings5
description: Gerencia configurações avançadas do cliente. Deriva da interface IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpClientAdvancedSettings5
- Serviços de Área de Trabalho Remota da interface IMsRdpClientAdvancedSettings5, descrita
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad2b26697cd3985cc0e39a8ed7345bc4bbe941
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622342"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a>Interface IMsRdpClientAdvancedSettings5

Gerencia configurações avançadas do cliente. Deriva da interface [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .

Para obter uma instância dessa interface, use a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obter um ponteiro de interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) . Em seguida, chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no ponteiro **IMsTscAdvancedSettings** e passe **\_ IMsRdpClientAdvancedSettings5 de IID** para **QueryInterface**.

## <a name="members"></a>Membros

A interface **IMsRdpClientAdvancedSettings5** herda de [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md). **IMsRdpClientAdvancedSettings5** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsRdpClientAdvancedSettings5** tem essas propriedades.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Propriedade</th>
<th >Tipo de acesso</th>
<th >Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a><br/></td>
<td >Leitura/gravação<br/></td>
<td >O modo de redirecionamento de áudio. A propriedade <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> tem os seguintes valores possíveis.<br/>
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (o redirecionamento de áudio está habilitado e a opção para redirecionamento é &quot; levada para este computador &quot; . Esse é o modo padrão.)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (o redirecionamento de áudio é habilitado e a opção é &quot; deixada no computador remoto &quot; . a &quot; opção deixar no computador remoto &quot; só tem suporte quando se conecta remotamente a um computador host que está executando o Windows Vista. se a conexão for para um computador host que esteja executando o Windows Server 2008, a opção &quot; deixar no computador remoto &quot; será alterada para &quot; não reproduzir &quot; .)<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (o redirecionamento de áudio está habilitado e o modo &quot; não é reproduzido &quot; .)<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a><br/></td>
<td >Leitura/gravação<br/></td>
<td >Especifica o tamanho do arquivo de cache virtual para bitmaps de 32 bits por pixel (BPP). O valor máximo é 48 megabytes (MB).<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a><br/></td>
<td >Leitura/gravação<br/></td>
<td >Especifica se o botão PIN deve ser mostrado na barra de conexão. Por padrão, o valor é <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>Públicomode</strong></a><br/></td>
<td >Leitura/gravação<br/></td>
<td >Especifica se o modo público deve ser habilitado ou desabilitado. Por padrão, o modo público é definido como <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a><br/></td>
<td >Leitura/gravação<br/></td>
<td >Especifica se o redirecionamento da área de transferência deve ser habilitado ou desabilitado. Por padrão, o modo de redirecionamento da área de transferência é definido como <strong>true</strong> (habilitado).<br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a><br/></td>
<td >Leitura/gravação<br/></td>
<td >Especifica se os dispositivos redirecionados devem ser habilitados ou desabilitados. Por padrão, o modo de dispositivos redirecionados é definido como <strong>false</strong>.<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a><br/></td>
<td >Leitura/gravação<br/></td>
<td >Especifica se os dispositivos redirecionados de ponto de serviço devem ser habilitados ou desabilitados. Por padrão, o modo de dispositivos redirecionados de ponto de serviço é definido como <strong>false</strong>.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 é definido como FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

