---
title: Constantes de TF_IAS_ (msctf. h)
description: As \_ constantes TF ias \_ \ são usadas como sinalizadores de campo de bits em métodos que inserem texto ou objetos inseridos em uma seleção ou ponto de inserção.
ms.assetid: adc5c539-fdb1-4829-ad17-2f54ec179c47
topic_type:
- apiref
api_name:
- TF_IAS_NOQUERY
- TF_IAS_QUERYONLY
- TF_IAS_NO_DEFAULT_COMPOSITION
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a025e295d80ac9a58625c221c4b4c224233fbb26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105792636"
---
# <a name="tf_ias_-constants"></a>TF \_ constantes do IAS \_ \*

As constantes do TF \_ ias \_ \* são usadas como sinalizadores de campo de bits em métodos que inserem texto ou objetos inseridos em uma seleção ou ponto de inserção.



| Constante/valor                                                                                                                                                                                                                                                                       | Descrição                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_IAS_NOQUERY"></span><span id="tf_ias_noquery"></span><dl> <dt>**TF \_ \_NoConsulta do IAS**</dt> <dt>(0x1)</dt> </dl>                                                       | O texto é inserido e o ponteiro de intervalo é definido como **nulo** na saída. Não pode ser combinado com o \_ sinalizador TF ias \_ QUERYONLY.<br/>       |
| <span id="TF_IAS_QUERYONLY"></span><span id="tf_ias_queryonly"></span><dl> <dt>**TF \_ \_QUERYONLY**</dt> <dt>(0X2) do</dt> ias </dl>                                                 | Não execute a inserção. O chamador requer apenas o ponteiro de intervalo a ser definido. Não pode ser combinado com o \_ sinalizador TF ias \_ noquery.<br/> |
| <span id="TF_IAS_NO_DEFAULT_COMPOSITION"></span><span id="tf_ias_no_default_composition"></span><dl> <dt>**TF \_ \_Nenhuma \_ \_ composição padrão do IAS**</dt> <dt>(0x80000000)</dt> </dl> | O TSF não criará uma composição padrão se uma composição for necessária. O chamador deve iniciar uma composição no intervalo.<br/>         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                 |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                      |
| parâmetro<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[ITextStoreACP:: InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-insertembeddedatselection)
</dt> <dt>

[ITextStoreACP:: InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-inserttextatselection)
</dt> <dt>

[ITextStoreAnchor::InsertEmbeddedAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-insertembeddedatselection)
</dt> <dt>

[ITextStoreAnchor::InsertTextAtSelection](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-inserttextatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertEmbeddedAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-insertembeddedatselection)
</dt> <dt>

[ITfInsertAtSelection::InsertTextAtSelection](/windows/desktop/api/Msctf/nf-msctf-itfinsertatselection-inserttextatselection)
</dt> </dl>

 

 





