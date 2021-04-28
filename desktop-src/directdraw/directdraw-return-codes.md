---
title: Códigos de retorno do DirectDraw (ddraw. h)
description: Códigos de retorno do DirectDraw-os erros são representados por valores negativos e não podem ser combinados.
ms.assetid: F713193E-3614-4741-B293-D312C170270A
topic_type:
- apiref
api_name:
- DD_OK
- DDERR_ALREADYINITIALIZED
- DDERR_BLTFASTCANTCLIP
- DDERR_CANNOTATTACHSURFACE
- DDERR_CANNOTDETACHSURFACE
- DDERR_CANTCREATEDC
- DDERR_CANTDUPLICATE
- DDERR_CANTLOCKSURFACE
- DDERR_CANTPAGELOCK
- DDERR_CANTPAGEUNLOCK
- DDERR_CLIPPERISUSINGHWND
- DDERR_COLORKEYNOTSET
- DDERR_CURRENTLYNOTAVAIL
- DDERR_DDSCAPSCOMPLEXREQUIRED
- DDERR_DCALREADYCREATED
- DDERR_DEVICEDOESNTOWNSURFACE
- DDERR_DIRECTDRAWALREADYCREATED
- DDERR_EXCEPTION
- DDERR_EXCLUSIVEMODEALREADYSET
- DDERR_EXPIRED
- DDERR_GENERIC
- DDERR_HEIGHTALIGN
- DDERR_HWNDALREADYSET
- DDERR_HWNDSUBCLASSED
- DDERR_IMPLICITLYCREATED
- DDERR_INCOMPATIBLEPRIMARY
- DDERR_INVALIDCAPS
- DDERR_INVALIDCLIPLIST
- DDERR_INVALIDDIRECTDRAWGUID
- DDERR_INVALIDMODE
- DDERR_INVALIDOBJECT
- DDERR_INVALIDPARAMS
- DDERR_INVALIDPIXELFORMAT
- DDERR_INVALIDPOSITION
- DDERR_INVALIDRECT
- DDERR_INVALIDSTREAM
- DDERR_INVALIDSURFACETYPE
- DDERR_LOCKEDSURFACES
- DDERR_MOREDATA
- DDERR_NEWMODE
- DDERR_NO3D
- DDERR_NOALPHAHW
- DDERR_NOBLTHW
- DDERR_NOCLIPLIST
- DDERR_NOCLIPPERATTACHED
- DDERR_NOCOLORCONVHW
- DDERR_NOCOLORKEY
- DDERR_NOCOLORKEYHW
- DDERR_NOCOOPERATIVELEVELSET
- DDERR_NODC
- DDERR_NODDROPSHW
- DDERR_NODIRECTDRAWHW
- DDERR_NODIRECTDRAWSUPPORT
- DDERR_NODRIVERSUPPORT
- DDERR_NOEMULATION
- DDERR_NOEXCLUSIVEMODE
- DDERR_NOFLIPHW
- DDERR_NOFOCUSWINDOW
- DDERR_NOGDI
- DDERR_NOHWND
- DDERR_NOMIPMAPHW
- DDERR_NOMIRRORHW
- DDERR_NOMONITORINFORMATION
- DDERR_NONONLOCALVIDMEM
- DDERR_NOOPTIMIZEHW
- DDERR_NOOVERLAYDEST
- DDERR_NOOVERLAYHW
- DDERR_NOPALETTEATTACHED
- DDERR_NOPALETTEHW
- DDERR_NORASTEROPHW
- DDERR_NOROTATIONHW
- DDERR_NOSTEREOHARDWARE
- DDERR_NOSTRETCHHW
- DDERR_NOSURFACELEFT
- DDERR_NOT4BITCOLOR
- DDERR_NOT4BITCOLORINDEX
- DDERR_NOT8BITCOLOR
- DDERR_NOTAOVERLAYSURFACE
- DDERR_NOTEXTUREHW
- DDERR_NOTFLIPPABLE
- DDERR_NOTFOUND
- DDERR_NOTINITIALIZED
- DDERR_NOTLOADED
- DDERR_NOTLOCKED
- DDERR_NOTPAGELOCKED
- DDERR_NOTPALETTIZED
- DDERR_NOVSYNCHW
- DDERR_NOZBUFFERHW
- DDERR_NOZOVERLAYHW
- DDERR_OUTOFCAPS
- DDERR_OUTOFMEMORY
- DDERR_OUTOFVIDEOMEMORY
- DDERR_OVERLAPPINGRECTS
- DDERR_OVERLAYCANTCLIP
- DDERR_OVERLAYCOLORKEYONLYONEACTIVE
- DDERR_OVERLAYNOTVISIBLE
- DDERR_PALETTEBUSY
- DDERR_PRIMARYSURFACEALREADYEXISTS
- DDERR_REGIONTOOSMALL
- DDERR_SURFACEALREADYATTACHED
- DDERR_SURFACEALREADYDEPENDENT
- DDERR_SURFACEBUSY
- DDERR_SURFACEISOBSCURED
- DDERR_SURFACELOST
- DDERR_SURFACENOTATTACHED
- DDERR_TESTFINISHED
- DDERR_TOOBIGHEIGHT
- DDERR_TOOBIGSIZE
- DDERR_TOOBIGWIDTH
- DDERR_UNSUPPORTED
- DDERR_UNSUPPORTEDFORMAT
- DDERR_UNSUPPORTEDMASK
- DDERR_UNSUPPORTEDMODE
- DDERR_VERTICALBLANKINPROGRESS
- DDERR_VIDEONOTACTIVE
- DDERR_WASSTILLDRAWING
- DDERR_WRONGMODE
- DDERR_XALIGN
api_location:
- Ddraw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d789a233df777d98860e519f7e877a030aba55a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087804"
---
# <a name="directdraw-return-codes"></a>Códigos de retorno do DirectDraw

Os erros são representados por valores negativos e não podem ser combinados. Esta tabela lista os valores que podem ser retornados por todos os métodos das [funções](directdraw-functions.md)do DirectDraw e das [interfaces do DirectDraw](directdraw-interfaces.md) . Para obter uma lista dos códigos de erro que cada método ou função pode retornar, consulte a descrição do método ou da função.

<dl> <dt>

<span id="DD_OK"></span><span id="dd_ok"></span>**DD \_ OK**
</dt> <dd> <dl> <dt>



A solicitação foi concluída com êxito.


</dt> </dl> </dd> <dt>

<span id="DDERR_ALREADYINITIALIZED"></span><span id="dderr_alreadyinitialized"></span>**DDERR \_ ALREADYINITIALIZED**
</dt> <dd> <dl> <dt>



O objeto já foi inicializado.


</dt> </dl> </dd> <dt>

<span id="DDERR_BLTFASTCANTCLIP"></span><span id="dderr_bltfastcantclip"></span>**DDERR \_ BLTFASTCANTCLIP**
</dt> <dd> <dl> <dt>



Um objeto DirectDrawClipper é anexado a uma superfície de origem que passou para uma chamada para o método [**IDirectDrawSurface7:: BltFast**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-bltfast) .


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTATTACHSURFACE"></span><span id="dderr_cannotattachsurface"></span>**DDERR \_ CANNOTATTACHSURFACE**
</dt> <dd> <dl> <dt>



Uma superfície não pode ser anexada a outra superfície solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANNOTDETACHSURFACE"></span><span id="dderr_cannotdetachsurface"></span>**DDERR \_ CANNOTDETACHSURFACE**
</dt> <dd> <dl> <dt>



Uma superfície não pode ser desanexada de outra superfície solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTCREATEDC"></span><span id="dderr_cantcreatedc"></span>**DDERR \_ CANTCREATEDC**
</dt> <dd> <dl> <dt>



O Windows não pode criar mais DCs (contextos de dispositivo) ou um controlador de domínio solicitou uma superfície indexada pela paleta quando a superfície não tinha nenhuma paleta e o modo de exibição não foi indexado pela paleta (nesse caso, o DirectDraw não pode selecionar uma paleta apropriada no controlador de domínio).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTDUPLICATE"></span><span id="dderr_cantduplicate"></span>**DDERR \_ CANTDUPLICATE**
</dt> <dd> <dl> <dt>



As superfícies primária e 3D, ou superfícies criadas implicitamente, não podem ser duplicadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTLOCKSURFACE"></span><span id="dderr_cantlocksurface"></span>**DDERR \_ CANTLOCKSURFACE**
</dt> <dd> <dl> <dt>



O acesso a essa superfície é recusado porque foi feita uma tentativa de bloquear a superfície primária sem suporte ao DCI (display Control interface).


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGELOCK"></span><span id="dderr_cantpagelock"></span>**DDERR \_ CANTPAGELOCK**
</dt> <dd> <dl> <dt>



Falha ao tentar bloquear paginação de página. O bloqueio de página não funciona em uma superfície de memória de exibição ou em uma superfície primária emulada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CANTPAGEUNLOCK"></span><span id="dderr_cantpageunlock"></span>**DDERR \_ CANTPAGEUNLOCK**
</dt> <dd> <dl> <dt>



Falha ao tentar destravar uma superfície na página. O desbloqueio de página não funciona em uma superfície de memória de exibição ou em uma superfície primária emulada.


</dt> </dl> </dd> <dt>

<span id="DDERR_CLIPPERISUSINGHWND"></span><span id="dderr_clipperisusinghwnd"></span>**DDERR \_ CLIPPERISUSINGHWND**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de definir uma lista de clipes para um objeto DirectDrawClipper que já está monitorando um identificador de janela.


</dt> </dl> </dd> <dt>

<span id="DDERR_COLORKEYNOTSET"></span><span id="dderr_colorkeynotset"></span>**DDERR \_ COLORKEYNOTSET**
</dt> <dd> <dl> <dt>



Nenhuma chave de cor de origem foi especificada para esta operação.


</dt> </dl> </dd> <dt>

<span id="DDERR_CURRENTLYNOTAVAIL"></span><span id="dderr_currentlynotavail"></span>**DDERR \_ CURRENTLYNOTAVAIL**
</dt> <dd> <dl> <dt>



Não há suporte disponível no momento.


</dt> </dl> </dd> <dt>

<span id="DDERR_DDSCAPSCOMPLEXREQUIRED"></span><span id="dderr_ddscapscomplexrequired"></span>**DDERR \_ DDSCAPSCOMPLEXREQUIRED**
</dt> <dd> <dl> <dt>



Novo no DirectX 7,0. A superfície requer o \_ sinalizador complexo DDSCAPS.


</dt> </dl> </dd> <dt>

<span id="DDERR_DCALREADYCREATED"></span><span id="dderr_dcalreadycreated"></span>**DDERR \_ DCALREADYCREATED**
</dt> <dd> <dl> <dt>



Um DC (contexto de dispositivo) já foi retornado para esta superfície. Somente um controlador de domínio pode ser recuperado para cada superfície.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DEVICEDOESNTOWNSURFACE"></span><span id="_dderr_devicedoesntownsurface"></span>**>DDERR \_ DEVICEDOESNTOWNSURFACE**
</dt> <dd> <dl> <dt>



As superfícies criadas por um dispositivo DirectDraw não podem ser usadas diretamente por outro dispositivo DirectDraw.


</dt> </dl> </dd> <dt>

<span id="_DDERR_DIRECTDRAWALREADYCREATED"></span><span id="_dderr_directdrawalreadycreated"></span>**>DDERR \_ DIRECTDRAWALREADYCREATED**
</dt> <dd> <dl> <dt>



Um objeto do DirectDraw que representa este driver já foi criado para esse processo.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCEPTION"></span><span id="dderr_exception"></span>**\_exceção DDERR**
</dt> <dd> <dl> <dt>



Exceção encontrada ao executar a operação solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXCLUSIVEMODEALREADYSET"></span><span id="dderr_exclusivemodealreadyset"></span>**DDERR \_ EXCLUSIVEMODEALREADYSET**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de definir o nível de cooperação quando ele já estava definido como exclusivo.


</dt> </dl> </dd> <dt>

<span id="DDERR_EXPIRED"></span><span id="dderr_expired"></span>**DDERR \_ expirou**
</dt> <dd> <dl> <dt>



Os dados expiraram e, portanto, não são mais válidos.


</dt> </dl> </dd> <dt>

<span id="DDERR_GENERIC"></span><span id="dderr_generic"></span>**DDERR \_ genérico**
</dt> <dd> <dl> <dt>



Há uma condição de erro indefinida.


</dt> </dl> </dd> <dt>

<span id="DDERR_HEIGHTALIGN"></span><span id="dderr_heightalign"></span>**DDERR \_ HEIGHTALIGN**
</dt> <dd> <dl> <dt>



A altura do retângulo fornecido não é um múltiplo do alinhamento necessário.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDALREADYSET"></span><span id="dderr_hwndalreadyset"></span>**DDERR \_ HWNDALREADYSET**
</dt> <dd> <dl> <dt>



O identificador de janela de nível cooperativo do DirectDraw já foi definido. Ele não pode ser redefinido enquanto o processo tem superfícies ou paletas criadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_HWNDSUBCLASSED"></span><span id="dderr_hwndsubclassed"></span>**DDERR \_ HWNDSUBCLASSED**
</dt> <dd> <dl> <dt>



O DirectDraw é impedido de restaurar o estado porque o identificador de janela de nível cooperativo do DirectDraw foi subclasse.


</dt> </dl> </dd> <dt>

<span id="DDERR_IMPLICITLYCREATED"></span><span id="dderr_implicitlycreated"></span>**DDERR \_ IMPLICITLYCREATED**
</dt> <dd> <dl> <dt>



A superfície não pode ser restaurada porque é uma superfície criada implicitamente.


</dt> </dl> </dd> <dt>

<span id="DDERR_INCOMPATIBLEPRIMARY"></span><span id="dderr_incompatibleprimary"></span>**DDERR \_ INCOMPATIBLEPRIMARY**
</dt> <dd> <dl> <dt>



A solicitação de criação de superfície primária não corresponde à superfície primária existente.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCAPS"></span><span id="dderr_invalidcaps"></span>**DDERR \_ INVALIDCAPS**
</dt> <dd> <dl> <dt>



Um ou mais dos bits de funcionalidade passados para a função de retorno de chamada estão incorretos.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDCLIPLIST"></span><span id="dderr_invalidcliplist"></span>**DDERR \_ INVALIDCLIPLIST**
</dt> <dd> <dl> <dt>



O DirectDraw não oferece suporte à lista de clipes fornecida.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDDIRECTDRAWGUID"></span><span id="dderr_invaliddirectdrawguid"></span>**DDERR \_ INVALIDDIRECTDRAWGUID**
</dt> <dd> <dl> <dt>



O GUID (identificador global exclusivo) passado para a função [**DirectDrawCreate**](/windows/desktop/api/Ddraw/nf-ddraw-directdrawcreate) não é um identificador de driver DirectDraw válido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDMODE"></span><span id="dderr_invalidmode"></span>**DDERR \_ INválidamode**
</dt> <dd> <dl> <dt>



O DirectDraw não oferece suporte ao modo solicitado.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDOBJECT"></span><span id="dderr_invalidobject"></span>**DDERR \_ INvalidaobject**
</dt> <dd> <dl> <dt>



O DirectDraw recebeu um ponteiro que era um objeto DirectDraw inválido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPARAMS"></span><span id="dderr_invalidparams"></span>**DDERR \_ INVALIDPARAMS**
</dt> <dd> <dl> <dt>



Um ou mais dos parâmetros passados para o método estão incorretos.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPIXELFORMAT"></span><span id="dderr_invalidpixelformat"></span>**DDERR \_ INVALIDPIXELFORMAT**
</dt> <dd> <dl> <dt>



O formato de pixel era inválido conforme especificado.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDPOSITION"></span><span id="dderr_invalidposition"></span>**DDERR \_ INVALIDPOSITION**
</dt> <dd> <dl> <dt>



A posição da sobreposição no destino não é mais válida.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDRECT"></span><span id="dderr_invalidrect"></span>**DDERR \_ INVALIDRECT**
</dt> <dd> <dl> <dt>



O retângulo fornecido era inválido.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSTREAM"></span><span id="dderr_invalidstream"></span>**DDERR \_ INVALIDSTREAM**
</dt> <dd> <dl> <dt>



O fluxo especificado contém dados inválidos.


</dt> </dl> </dd> <dt>

<span id="DDERR_INVALIDSURFACETYPE"></span><span id="dderr_invalidsurfacetype"></span>**DDERR \_ INVALIDSURFACETYPE**
</dt> <dd> <dl> <dt>



A superfície era do tipo incorreto.


</dt> </dl> </dd> <dt>

<span id="DDERR_LOCKEDSURFACES"></span><span id="dderr_lockedsurfaces"></span>**DDERR \_ LOCKEDSURFACES**
</dt> <dd> <dl> <dt>



Uma ou mais superfícies estão bloqueadas, causando a falha da operação solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_MOREDATA"></span><span id="dderr_moredata"></span>**DDERR \_ MOREDATA**
</dt> <dd> <dl> <dt>



Há mais dados disponíveis do que o tamanho de buffer especificado pode conter.


</dt> </dl> </dd> <dt>

<span id="DDERR_NEWMODE"></span><span id="dderr_newmode"></span>**DDERR \_ NewMode**
</dt> <dd> <dl> <dt>



Novo no DirectX 7,0. Quando [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) é chamado com o \_ sinalizador DDSMT ISTESTREQUIRED, ele pode retornar esse valor para indicar que algumas ou todas as resoluções podem e devem ser testadas. [**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode) retorna esse valor para indicar que o teste mudou para um novo modo de exibição.


</dt> </dl> </dd> <dt>

<span id="DDERR_NO3D"></span><span id="dderr_no3d"></span>**DDERR \_ NO3D**
</dt> <dd> <dl> <dt>



Nenhum hardware 3D ou emulação está presente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOALPHAHW"></span><span id="dderr_noalphahw"></span>**DDERR \_ NOALPHAHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de aceleração alfa está presente ou disponível, causando a falha da operação solicitada.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOBLTHW"></span><span id="dderr_noblthw"></span>**DDERR \_ NOBLTHW**
</dt> <dd> <dl> <dt>



Nenhum bloco de bits transferindo o hardware está presente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPLIST"></span><span id="dderr_nocliplist"></span>**DDERR \_ NOmedialist**
</dt> <dd> <dl> <dt>



Nenhuma lista de clipes disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCLIPPERATTACHED"></span><span id="dderr_noclipperattached"></span>**DDERR \_ NOCLIPPERATTACHED**
</dt> <dd> <dl> <dt>



Nenhum objeto DirectDrawClipper está anexado ao objeto Surface.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORCONVHW"></span><span id="dderr_nocolorconvhw"></span>**DDERR \_ NOCOLORCONVHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de conversão de cor está presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEY"></span><span id="dderr_nocolorkey"></span>**DDERR \_ NOCOLORKEY**
</dt> <dd> <dl> <dt>



A superfície não tem uma chave de cor no momento.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOLORKEYHW"></span><span id="dderr_nocolorkeyhw"></span>**DDERR \_ NOCOLORKEYHW**
</dt> <dd> <dl> <dt>



Não há suporte de hardware para a chave de cor de destino.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOCOOPERATIVELEVELSET"></span><span id="dderr_nocooperativelevelset"></span>**DDERR \_ NOCOOPERATIVELEVELSET**
</dt> <dd> <dl> <dt>



Uma função CREATE foi chamada sem o método [**IDirectDraw7:: SetCooperativeLevel**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-setcooperativelevel) .


</dt> </dl> </dd> <dt>

<span id="DDERR_NODC"></span><span id="dderr_nodc"></span>**DDERR \_ NODC**
</dt> <dd> <dl> <dt>



Nenhum contexto de dispositivo (DC) já foi criado para esta superfície.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODDROPSHW"></span><span id="dderr_noddropshw"></span>**DDERR \_ NODDROPSHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de operação de varredura (ROP) do DirectDraw está disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWHW"></span><span id="dderr_nodirectdrawhw"></span>**DDERR \_ NODIRECTDRAWHW**
</dt> <dd> <dl> <dt>



A criação de objeto DirectDraw somente de hardware não é possível; o driver não oferece suporte a nenhum hardware.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODIRECTDRAWSUPPORT"></span><span id="dderr_nodirectdrawsupport"></span>**DDERR \_ NODIRECTDRAWSUPPORT**
</dt> <dd> <dl> <dt>



O suporte do DirectDraw não é possível com o driver de vídeo atual.


</dt> </dl> </dd> <dt>

<span id="DDERR_NODRIVERSUPPORT"></span><span id="dderr_nodriversupport"></span>**DDERR \_ NODRIVERSUPPORT**
</dt> <dd> <dl> <dt>



Novo no DirectX 7,0. O teste não pode continuar porque o driver do adaptador de vídeo não enumera taxas de atualização.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEMULATION"></span><span id="dderr_noemulation"></span>**DDERR \_ NOemulação**
</dt> <dd> <dl> <dt>



A emulação de software não está disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOEXCLUSIVEMODE"></span><span id="dderr_noexclusivemode"></span>**DDERR \_ NOexcludemode**
</dt> <dd> <dl> <dt>



A operação requer que o aplicativo tenha o modo exclusivo, mas o aplicativo não tem modo exclusivo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFLIPHW"></span><span id="dderr_nofliphw"></span>**DDERR \_ NOFLIPHW**
</dt> <dd> <dl> <dt>



Não há suporte para a inversão de superfícies visíveis.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOFOCUSWINDOW"></span><span id="dderr_nofocuswindow"></span>**DDERR \_ NOFOCUSWINDOW**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de criar ou definir uma janela do dispositivo sem primeiro definir a janela de foco.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOGDI"></span><span id="dderr_nogdi"></span>**DDERR \_ NOGDI**
</dt> <dd> <dl> <dt>



Não há GDI presente.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOHWND"></span><span id="dderr_nohwnd"></span>**DDERR \_ NOhwnd**
</dt> <dd> <dl> <dt>



A notificação do Clipper requer um identificador de janela ou nenhum identificador de janela foi definido anteriormente como o identificador de janela de nível cooperativo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIPMAPHW"></span><span id="dderr_nomipmaphw"></span>**DDERR \_ NOMIPMAPHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de mapeamento de textura compatível com mipmap está presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMIRRORHW"></span><span id="dderr_nomirrorhw"></span>**DDERR \_ NOMIRRORHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de espelhamento está presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOMONITORINFORMATION"></span><span id="dderr_nomonitorinformation"></span>**DDERR \_ NOMONITORINFORMATION**
</dt> <dd> <dl> <dt>



Novo no DirectX 7,0. O teste não pode continuar porque o monitor não tem dados EDID associados.


</dt> </dl> </dd> <dt>

<span id="DDERR_NONONLOCALVIDMEM"></span><span id="dderr_nononlocalvidmem"></span>**DDERR \_ NONONLOCALVIDMEM**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de alocar memória de vídeo não local de um dispositivo que não dá suporte à memória de vídeo não local.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOPTIMIZEHW"></span><span id="dderr_nooptimizehw"></span>**DDERR \_ NOOPTIMIZEHW**
</dt> <dd> <dl> <dt>



O dispositivo não dá suporte a superfícies otimizadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYDEST"></span><span id="dderr_nooverlaydest"></span>**DDERR \_ NOOVERLAYDEST**
</dt> <dd> <dl> <dt>



O método [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) é chamado em uma sobreposição que o método [**IDirectDrawSurface7:: UpdateOverlay**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-updateoverlay) não foi chamado para estabelecer como destino.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOOVERLAYHW"></span><span id="dderr_nooverlayhw"></span>**DDERR \_ NOOVERLAYHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de sobreposição está presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEATTACHED"></span><span id="dderr_nopaletteattached"></span>**DDERR \_ NOPALETTEATTACHED**
</dt> <dd> <dl> <dt>



Nenhum objeto de paleta está anexado a esta superfície.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOPALETTEHW"></span><span id="dderr_nopalettehw"></span>**DDERR \_ NOPALETTEHW**
</dt> <dd> <dl> <dt>



Não há suporte de hardware para paletas de 16 ou 256 cores.


</dt> </dl> </dd> <dt>

<span id="DDERR_NORASTEROPHW"></span><span id="dderr_norasterophw"></span>**DDERR \_ NORASTEROPHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de operação de varredura apropriado está presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOROTATIONHW"></span><span id="dderr_norotationhw"></span>**DDERR \_ NOROTATIONHW**
</dt> <dd> <dl> <dt>



Nenhum hardware de rotação está presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTEREOHARDWARE"></span><span id="dderr_nostereohardware"></span>**DDERR \_ NOSTEREOHARDWARE**
</dt> <dd> <dl> <dt>



Não há nenhum hardware estéreo presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSTRETCHHW"></span><span id="dderr_nostretchhw"></span>**DDERR \_ NOSTRETCHHW**
</dt> <dd> <dl> <dt>



Não há suporte de hardware para alongamento.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOSURFACELEFT"></span><span id="dderr_nosurfaceleft"></span>**DDERR \_ NOSURFACELEFT**
</dt> <dd> <dl> <dt>



Não há nenhum hardware presente que dê suporte a superfícies estéreo.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLOR"></span><span id="dderr_not4bitcolor"></span>**DDERR \_ NOT4BITCOLOR**
</dt> <dd> <dl> <dt>



O objeto DirectDrawSurface não está usando uma paleta de cores de 4 bits e a operação solicitada requer uma paleta de cores de 4 bits.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT4BITCOLORINDEX"></span><span id="dderr_not4bitcolorindex"></span>**DDERR \_ NOT4BITCOLORINDEX**
</dt> <dd> <dl> <dt>



O objeto DirectDrawSurface não está usando uma paleta de índice de cores de 4 bits e a operação solicitada requer uma paleta de índice de cores de 4 bits.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOT8BITCOLOR"></span><span id="dderr_not8bitcolor"></span>**DDERR \_ NOT8BITCOLOR**
</dt> <dd> <dl> <dt>



O objeto DirectDrawSurface não está usando uma paleta de cores de 8 bits e a operação solicitada requer uma paleta de cores de 8 bits.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTAOVERLAYSURFACE"></span><span id="dderr_notaoverlaysurface"></span>**DDERR \_ NOTAOVERLAYSURFACE**
</dt> <dd> <dl> <dt>



Um componente de sobreposição é chamado para uma superfície não sobreposta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTEXTUREHW"></span><span id="dderr_notexturehw"></span>**DDERR \_ NOTEXTUREHW**
</dt> <dd> <dl> <dt>



A operação não pode ser executada porque nenhum hardware de mapeamento de textura está presente ou disponível.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFLIPPABLE"></span><span id="dderr_notflippable"></span>**DDERR não \_ INverteble**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de virar uma superfície que não pode ser invertida.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTFOUND"></span><span id="dderr_notfound"></span>**DDERR não \_ encontrado**
</dt> <dd> <dl> <dt>



O item solicitado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTINITIALIZED"></span><span id="dderr_notinitialized"></span>**DDERR não \_ inicializado**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de chamar um método de interface de um objeto DirectDraw criado por [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) antes da inicialização do objeto.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOADED"></span><span id="dderr_notloaded"></span>**DDERR não \_ carregado**
</dt> <dd> <dl> <dt>



A superfície é uma superfície otimizada, mas ainda não foi alocada nenhuma memória.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTLOCKED"></span><span id="dderr_notlocked"></span>**DDERR não \_ bloqueado**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de desbloquear uma superfície que não estava bloqueada.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPAGELOCKED"></span><span id="dderr_notpagelocked"></span>**DDERR \_ NOTPAGELOCKED**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de desbloquear a página em uma superfície sem bloqueios de página pendentes.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOTPALETTIZED"></span><span id="dderr_notpalettized"></span>**DDERR \_ NOTPALETTIZED**
</dt> <dd> <dl> <dt>



A superfície que está sendo usada não é uma superfície baseada em paleta.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOVSYNCHW"></span><span id="dderr_novsynchw"></span>**DDERR \_ NOVSYNCHW**
</dt> <dd> <dl> <dt>



Não há suporte de hardware para operações verticais em branco sincronizadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZBUFFERHW"></span><span id="dderr_nozbufferhw"></span>**DDERR \_ NOZBUFFERHW**
</dt> <dd> <dl> <dt>



A operação para criar um z-buffer na memória de vídeo ou executar uma transferência de bloco de bits (BitBlt), usando um z-buffer não pode ser executada porque não há suporte de hardware para z-buffers.


</dt> </dl> </dd> <dt>

<span id="DDERR_NOZOVERLAYHW"></span><span id="dderr_nozoverlayhw"></span>**DDERR \_ NOZOVERLAYHW**
</dt> <dd> <dl> <dt>



As superfícies de sobreposição não podem ser em camadas z, com base na ordem z, porque o hardware não dá suporte à ordenação z de sobreposições.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFCAPS"></span><span id="dderr_outofcaps"></span>**DDERR \_ OUTOFCAPS**
</dt> <dd> <dl> <dt>



O hardware necessário para a operação solicitada já foi alocado.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFMEMORY"></span><span id="dderr_outofmemory"></span>**\_OUTOFMEMORY DDERR**
</dt> <dd> <dl> <dt>



O DirectDraw não tem memória suficiente para executar a operação.


</dt> </dl> </dd> <dt>

<span id="DDERR_OUTOFVIDEOMEMORY"></span><span id="dderr_outofvideomemory"></span>**DDERR \_ OUTOFVIDEOMEMORY**
</dt> <dd> <dl> <dt>



O DirectDraw não tem memória de vídeo suficiente para executar a operação.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAPPINGRECTS"></span><span id="dderr_overlappingrects"></span>**DDERR \_ OVERLAPPINGRECTS**
</dt> <dd> <dl> <dt>



Os retângulos de origem e de destino estão na mesma superfície e se sobrepõem.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCANTCLIP"></span><span id="dderr_overlaycantclip"></span>**DDERR \_ OVERLAYCANTCLIP**
</dt> <dd> <dl> <dt>



O hardware não oferece suporte a sobreposições recortadas.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYCOLORKEYONLYONEACTIVE"></span><span id="dderr_overlaycolorkeyonlyoneactive"></span>**DDERR \_ OVERLAYCOLORKEYONLYONEACTIVE**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de ter mais de uma chave de cor ativa em uma sobreposição.


</dt> </dl> </dd> <dt>

<span id="DDERR_OVERLAYNOTVISIBLE"></span><span id="dderr_overlaynotvisible"></span>**DDERR \_ OVERLAYNOTVISIBLE**
</dt> <dd> <dl> <dt>



O método [**IDirectDrawSurface7:: GetOverlayPosition**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-getoverlayposition) foi chamado em uma sobreposição oculta.


</dt> </dl> </dd> <dt>

<span id="DDERR_PALETTEBUSY"></span><span id="dderr_palettebusy"></span>**DDERR \_ PALETTEBUSY**
</dt> <dd> <dl> <dt>



O acesso a esta paleta foi recusado porque a paleta está bloqueada por outro thread.


</dt> </dl> </dd> <dt>

<span id="DDERR_PRIMARYSURFACEALREADYEXISTS"></span><span id="dderr_primarysurfacealreadyexists"></span>**DDERR \_ PRIMARYSURFACEALREADYEXISTS**
</dt> <dd> <dl> <dt>



Este processo já criou uma superfície primária.


</dt> </dl> </dd> <dt>

<span id="DDERR_REGIONTOOSMALL"></span><span id="dderr_regiontoosmall"></span>**DDERR \_ REGIONTOOSMALL**
</dt> <dd> <dl> <dt>



A região passada para o método [**IDirectDrawClipper:: Getmedialist**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawclipper-getcliplist) é muito pequena.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYATTACHED"></span><span id="dderr_surfacealreadyattached"></span>**DDERR \_ SURFACEALREADYATTACHED**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de anexar uma superfície a outra superfície à qual ela já está anexada.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEALREADYDEPENDENT"></span><span id="dderr_surfacealreadydependent"></span>**DDERR \_ SURFACEALREADYDEPENDENT**
</dt> <dd> <dl> <dt>



Foi feita uma tentativa de tornar uma superfície uma dependência de outra superfície na qual ela já é dependente.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEBUSY"></span><span id="dderr_surfacebusy"></span>**DDERR \_ SURFACEBUSY**
</dt> <dd> <dl> <dt>



O acesso à superfície é recusado porque a superfície está bloqueada por outro thread.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACEISOBSCURED"></span><span id="dderr_surfaceisobscured"></span>**DDERR \_ SURFACEISOBSCURED**
</dt> <dd> <dl> <dt>



O acesso à superfície é recusado porque a superfície está obscurecida.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACELOST"></span><span id="dderr_surfacelost"></span>**DDERR \_ SURFACELOST**
</dt> <dd> <dl> <dt>



O acesso à superfície é recusado porque a memória da superfície não existe mais. Chame o método [**IDirectDrawSurface7:: Restore**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdrawsurface7-restore) nesta superfície para restaurar a memória associada a ele.


</dt> </dl> </dd> <dt>

<span id="DDERR_SURFACENOTATTACHED"></span><span id="dderr_surfacenotattached"></span>**DDERR \_ SURFACENOTATTACHED**
</dt> <dd> <dl> <dt>



A superfície solicitada não está anexada.


</dt> </dl> </dd> <dt>

<span id="DDERR_TESTFINISHED"></span><span id="dderr_testfinished"></span>**DDERR \_ TESTFINISHED**
</dt> <dd> <dl> <dt>



Novo no DirectX 7,0. Quando retornado pelo método [**IDirectDraw7:: StartModeTest**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-startmodetest) , esse valor significa que nenhum teste pôde ser iniciado porque todas as resoluções escolhidas para teste já têm informações de taxa de atualização no registro. Quando retornado por [**IDirectDraw7:: evaluatemode**](/windows/desktop/api/Ddraw/nf-ddraw-idirectdraw7-evaluatemode), o valor significa que o DirectDraw concluiu um teste de taxa de atualização.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGHEIGHT"></span><span id="dderr_toobigheight"></span>**DDERR \_ TOOBIGHEIGHT**
</dt> <dd> <dl> <dt>



A altura solicitada pelo DirectDraw é muito grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGSIZE"></span><span id="dderr_toobigsize"></span>**DDERR \_ TOOBIGSIZE**
</dt> <dd> <dl> <dt>



O tamanho solicitado pelo DirectDraw é muito grande. No entanto, a altura e a largura individuais são tamanhos válidos.


</dt> </dl> </dd> <dt>

<span id="DDERR_TOOBIGWIDTH"></span><span id="dderr_toobigwidth"></span>**DDERR \_ TOOBIGWIDTH**
</dt> <dd> <dl> <dt>



A largura solicitada pelo DirectDraw é muito grande.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTED"></span><span id="dderr_unsupported"></span>**DDERR \_ sem suporte**
</dt> <dd> <dl> <dt>



A operação não tem suporte.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDFORMAT"></span><span id="dderr_unsupportedformat"></span>**DDERR \_ UNSUPPORTEDFORMAT**
</dt> <dd> <dl> <dt>



Não há suporte para o formato de pixel solicitado pelo DirectDraw.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMASK"></span><span id="dderr_unsupportedmask"></span>**DDERR \_ UNSUPPORTEDMASK**
</dt> <dd> <dl> <dt>



O DirectDraw não dá suporte ao bitmask no formato de pixel solicitado.


</dt> </dl> </dd> <dt>

<span id="DDERR_UNSUPPORTEDMODE"></span><span id="dderr_unsupportedmode"></span>**DDERR \_ sem suporte**
</dt> <dd> <dl> <dt>



A exibição está atualmente em um modo sem suporte.


</dt> </dl> </dd> <dt>

<span id="DDERR_VERTICALBLANKINPROGRESS"></span><span id="dderr_verticalblankinprogress"></span>**DDERR \_ VERTICALBLANKINPROGRESS**
</dt> <dd> <dl> <dt>



Uma vertical em branco está em andamento.


</dt> </dl> </dd> <dt>

<span id="DDERR_VIDEONOTACTIVE"></span><span id="dderr_videonotactive"></span>**DDERR \_ VIDEONOTACTIVE**
</dt> <dd> <dl> <dt>



A porta de vídeo não está ativa.


</dt> </dl> </dd> <dt>

<span id="DDERR_WASSTILLDRAWING"></span><span id="dderr_wasstilldrawing"></span>**DDERR \_ WASSTILLDRAWING**
</dt> <dd> <dl> <dt>



A operação BitBlt anterior que está transferindo informações para ou desta superfície está incompleta.


</dt> </dl> </dd> <dt>

<span id="DDERR_WRONGMODE"></span><span id="dderr_wrongmode"></span>**DDERR \_ incorretomode**
</dt> <dd> <dl> <dt>



Esta superfície não pode ser restaurada porque foi criada em um modo diferente.


</dt> </dl> </dd> <dt>

<span id="DDERR_XALIGN"></span><span id="dderr_xalign"></span>**DDERR \_ XALIGN**
</dt> <dd> <dl> <dt>



O retângulo fornecido não estava alinhado horizontalmente em um limite necessário.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

