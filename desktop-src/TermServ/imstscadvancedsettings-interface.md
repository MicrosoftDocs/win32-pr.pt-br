---
title: Interface IMsTscAdvancedSettings
description: Inclui métodos para recuperar e definir propriedades que habilitam o cache de bitmaps, a compactação e a impressora e o redirecionamento de área de transferência.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota da interface IMsTscAdvancedSettings, descrita
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f1156f59178275ff9406299fc553afacd3ce99a0488497f836d147ec1d63547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118606193"
---
# <a name="imstscadvancedsettings-interface"></a>Interface IMsTscAdvancedSettings

Inclui métodos para recuperar e definir propriedades que habilitam o cache de bitmaps, a compactação e a impressora e o redirecionamento de área de transferência. Você também pode especificar nomes de DLLs de cliente do canal virtual.

Você Obtém uma instância dessa interface usando a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) .

## <a name="members"></a>Membros

A interface **IMsTscAdvancedSettings** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IMsTscAdvancedSettings** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **IMsTscAdvancedSettings** tem essas propriedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriedade</th>
<th style="text-align: left;">Tipo de acesso</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se o modo de entrada em segundo plano está habilitado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se o cache de bitmaps está habilitado.<br/>
<blockquote>
[!Note]<br />
O erro ortográfico no nome da propriedade está na versão liberada do controle.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-compress.md"><strong>Compactar</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se a compactação está habilitada.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se o modo de tela inteira manipulado por contêiner está habilitado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a><br/></td>
<td style="text-align: left;">Leitura/gravação<br/></td>
<td style="text-align: left;">Especifica se a impressora e o redirecionamento de área de transferência estão habilitados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconfile.md"><strong>Ícone</strong></a><br/></td>
<td style="text-align: left;">Somente gravação<br/></td>
<td style="text-align: left;">Especifica o nome do arquivo que contém os dados de ícone que serão acessados ao exibir o cliente no modo de tela inteira.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a><br/></td>
<td style="text-align: left;">Somente gravação<br/></td>
<td style="text-align: left;">Especifica o índice do ícone dentro do arquivo de ícone atual.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a><br/></td>
<td style="text-align: left;">Somente gravação<br/></td>
<td style="text-align: left;">Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout de teclado) a ser usado para a conexão.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a><br/></td>
<td style="text-align: left;">Somente gravação<br/></td>
<td style="text-align: left;">Especifica os nomes das DLLs de cliente do canal virtual a serem carregadas.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
-   [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
-   [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
-   [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
-   [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)

Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>    |
| IID<br/>                      | IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[Referência de Conexão Web de Área de Trabalho Remota](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

