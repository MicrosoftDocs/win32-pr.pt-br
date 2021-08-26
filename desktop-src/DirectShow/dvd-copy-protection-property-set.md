---
description: O conjunto de propriedades proteção de cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software. Use essa propriedade definida para impedir a cópia não autorizada do DVD-Video pré-gravado.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propriedades da proteção contra cópia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76034c0ac9b310d446f142d31b96ea2edbe6b725
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477342"
---
# <a name="dvd-copy-protection-property-set"></a>Conjunto de propriedades de proteção de cópia de DVD

O conjunto de propriedades proteção de cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software. Use essa propriedade definida para impedir a cópia não autorizada do DVD-Video pré-gravado.

A Microsoft fornece software que facilita o processo de autenticação exigido pelo esquema de criptografia, permitindo que uma unidade de DVD-ROM autententure e transfira chaves com um descriptografador de DVD. A Microsoft não tem planos atuais para enviar um descriptografador de DVD e, em vez disso, está fornecendo código do sistema operacional que atuará como o agente para habilitar a autenticação de descriptografadores de hardware ou software.

O navegador de DVD inicia e controla o processo de troca de chaves. O minidriver de DVD só precisa implementar as propriedades a seguir. Outros componentes lidam com o restante.

Cada fluxo de entrada de DVD receberá propriedades de proteção de cópia. Isso é verdadeiro mesmo que o mesmo hardware controle todos os fluxos de DVD.

As informações a seguir apresentam as constantes e os tipos de dados necessários a usar para esse conjunto de propriedades em chamadas para [**métodos IKsPropertySet.**](ikspropertyset.md) Ele fornece valores para os parâmetros **GUID** (*guidPropSet),* iD da propriedade (*dwPropID*) e tipo de dados de propriedade (*pPropData*).



| Rótulo | Valor |
|-------------------|---------------------------|
| GUID do Conjunto de Propriedades | AM \_ KSPROPSETID \_ CopyProt |



 




| ID da propriedade | Descrição | 
|-------------|-------------|
| <a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a> | Consulta se a saída do vídeo é de definição padrão, vídeo de componente análogo. | 
| AM_PROPERTY_COPY_MACROVISION | Essa é uma propriedade somente definida. Essa propriedade define o nível de proteção de cópia análoga para o codificador NTSC na extremidade de saída do pino de recebimento. Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>. | 
| AM_PROPERTY_DVDCOPY_CHLG_KEY | Há suporte para operações get e set nessa propriedade. Uma operação get solicita que o decodificador forneça sua chave de desafio do barramento. Uma operação de conjunto fornece ao decodificador a chave de desafio do barramento da unidade de DVD. Os dados passados nesta propriedade serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DEC_KEY2 | Essa é uma propriedade get-only. Essa propriedade solicita que a chave 2 do barramento do decodificador seja transferida para a unidade de DVD. Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DISC_KEY | Propriedade somente definida. Isso fornece a chave de disco. A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_DVD_KEY1 | Essa é uma propriedade somente definida. Essa propriedade fornece a chave de barramento de unidade de DVD 1 para o decodificador. Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>. | 
| AM_PROPERTY_DVDCOPY_REGION | O código de região solicita a definição de região em que o decodificador tem permissão para reproduzir conforme definido pelo consórcio de DVD. Essa região é definida como uma <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>estrutura DVD_REGION</strong></a> dados. | 
| AM_PROPERTY_DVDCOPY_SET_COPY_STATE | Há suporte para get e set nessa propriedade. Get é chamado primeiro para determinar se a autenticação é necessária. As propriedades de conjunto são indicações de qual fase de negociação de proteção de cópia o filtro está inserindo. Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>. | 
| AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT | Se essa propriedade for <strong>TRUE,</strong>o Navegador de DVD não enviará <strong>AM_UseNewCSSKey</strong> exemplos antes de negociar a chave de disco. Consulte <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br /> Somente leitura. Os dados da propriedade são um <strong>valor BOOL.</strong><br /><blockquote>[!Note]<br />Aplica-se Windows 7.</blockquote><br /> | 
| AM_PROPERTY_DVDCOPY_TITLE_KEY | Essa é uma propriedade somente definida. Isso fornece a chave de título do conteúdo atual. A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>. | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




