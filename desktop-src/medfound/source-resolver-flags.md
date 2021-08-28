---
description: Define o comportamento do resolvedor de origem. Esses sinalizadores também são usados por manipuladores de esquema e manipuladores de fluxo de bytes.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Sinalizadores do resolvedor de origem (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c779a54467390abf6cfb186f6b76043fd19617f5d129b88e6697a45c01708510
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847816"
---
# <a name="source-resolver-flags"></a>Sinalizadores do resolvedor de origem

Define o comportamento do resolvedor de origem. Esses sinalizadores também são usados por manipuladores de esquema e manipuladores de fluxo de bytes.



| Constante/valor                                                                                                                                                                                                                                                                                                                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ \_Mediation de resolução**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | Tentativa de criar uma origem de mídia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ RESOLUÇÃO \_ bytes**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                              | Tentativa de criar um fluxo de bytes.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> <dt> **\_ \_ O conteúdo de resolução MF \_ \_ não \_ precisa \_ corresponder à \_ \_ extensão \_ ou ao \_ \_ tipo MIME**</dt> <dt>0x00000010</dt> </dl> | Se a resolução de origem falhar usando o manipulador de fluxo de bytes registrado para o tipo MIME ou extensão de nome de arquivo, o resolvedor de origem enumerará todos os manipuladores de fluxo de bytes registrados.<br/> Os manipuladores de fluxo de bytes são registrados por extensão de nome de arquivo ou tipo MIME. Inicialmente, o resolvedor de origem tenta usar um manipulador que corresponda à extensão de nome de arquivo ou ao tipo MIME. Se isso falhar, por padrão, a resolução de origem inteira falhará e o resolvedor de origem retornará um código de erro para o aplicativo. No entanto, se esse sinalizador for especificado, o resolvedor de origem continuará enumerando por todos os manipuladores de fluxo de bytes registrados. Possivelmente um manipulador com correspondência incorreta pode criar com êxito a origem da mídia.<br/> Esse sinalizador não pode ser combinado com o \_ sinalizador manter a resolução de \_ \_ bytes \_ \_ \_ em funcionamento no fluxo de \_ falha. Consulte comentários para obter mais informações.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ RESOLUÇÃO \_ manter \_ o \_ fluxo \_ de bytes ativo \_ na \_ falha**</dt> <dt>0x00000020</dt> </dl>                                                                             | Se a resolução da origem falhar, o resolvedor de origem não fechará o fluxo de bytes. Por padrão, o resolvedor de origem fecha o fluxo de bytes em caso de falha.<br/> Se esse sinalizador for usado e a resolução de origem falhar, o chamador deverá chamar o método novamente e definir o \_ conteúdo de resolução MF \_ \_ \_ não \_ precisa \_ corresponder à \_ \_ extensão ou ao \_ sinalizador de \_ \_ tipo MIME.<br/> Esse sinalizador não pode ser combinado com o \_ conteúdo de resolução MF \_ \_ \_ não \_ precisa \_ corresponder à \_ \_ extensão \_ ou ao sinalizador de \_ \_ tipo MIME. Consulte comentários para obter mais informações.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ 0x00010000 de \_ leitura de resolução**</dt> <dt></dt> </dl>                                                                                                                                                                | Solicita acesso de leitura à origem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ 0x00020000 de \_ gravação de resolução**</dt> <dt></dt> </dl>                                                                                                                                                             | Solicita acesso de gravação à origem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ RESOLUÇÃO \_ desabilite os \_ \_ plug-ins locais**</dt> <dt>0x00000040</dt> </dl>                                                                                                           | O resolvedor de origem não usará o esquema registrado localmente ou os plug-ins do manipulador bytes.<br/> Requer Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Comentários

O aplicativo define esses sinalizadores quando ele usa a interface [**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) . O resolvedor de origem passa os mesmos sinalizadores para os métodos [**IMFByteStreamHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) e [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject) .

Você deve especificar um dos sinalizadores bytes da resolução MF \_ \_ ou MF \_ \_ . Os sinalizadores restantes são todos opcionais.

O \_ sinalizador manter a resolução de \_ \_ bytes \_ \_ em funcionamento no fluxo de \_ \_ falha é definido para o seguinte cenário:

1.  O aplicativo tenta abrir uma fonte pela rede. O aplicativo define a resolução de MF \_ \_ manter o fluxo de \_ bytes \_ \_ \_ em funcionamento no \_ sinalizador de falha.

2.  A URL da origem contém a extensão de nome de arquivo incorreta. Como a extensão de nome de arquivo está errada, o manipulador de fluxo de bytes padrão não pode criar a origem da mídia. Como o aplicativo definiu a \_ resolução de MF \_ manter o fluxo de \_ bytes \_ \_ ativo \_ no \_ sinalizador de falha, o resolvedor de origem armazena em cache o fluxo de bytes.

3.  O resolvedor de origem retorna um código de erro para o aplicativo.

4.  O cliente abre a origem novamente, desta vez, a configuração do \_ conteúdo de resolução MF \_ \_ \_ não \_ precisa corresponder à \_ \_ \_ extensão ou ao sinalizador de \_ \_ \_ tipo MIME. Esse sinalizador faz com que o resolvedor de origem Experimente todos os manipuladores registrados em vez de apenas o manipulador padrão. Como o fluxo de bytes foi armazenado em cache, o resolvedor de origem não precisa abrir o fluxo de bytes novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation constantes](media-foundation-constants.md)
</dt> <dt>

[**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMFSourceResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Resolvedor de origem](source-resolver.md)
</dt> </dl>

 

 




