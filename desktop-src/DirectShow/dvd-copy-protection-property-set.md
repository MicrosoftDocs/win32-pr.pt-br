---
description: O conjunto de propriedades proteção contra cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software. Use este conjunto de propriedades para impedir a cópia não autorizada de DVD-Video pré-gravados.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: Conjunto de propriedades da proteção contra cópia de DVD (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810237"
---
# <a name="dvd-copy-protection-property-set"></a>Conjunto de propriedades da proteção contra cópia de DVD

O conjunto de propriedades proteção contra cópia de DVD fornece autenticação de informações de proteção de cópia de descriptografadores de hardware ou software. Use este conjunto de propriedades para impedir a cópia não autorizada de DVD-Video pré-gravados.

A Microsoft fornece software que facilita o processo de autenticação exigido pelo esquema de criptografia, permitindo, assim, uma unidade de DVD-ROM para autenticar e transferir chaves com um DVD Decrypter. A Microsoft não tem planos atuais para enviar um DVD Decrypter e, em vez disso, está fornecendo código do sistema operacional que atuará como agente para habilitar a autenticação de descriptografadores de hardware ou software.

O navegador de DVD inicia e controla o processo de troca de chaves. O DVD minidriver precisa apenas implementar as propriedades a seguir. Outros componentes manipulam o restante.

Cada fluxo de entrada de DVD receberá Propriedades de proteção de cópia. Isso é verdadeiro mesmo que o mesmo hardware controle todos os fluxos de DVD.

As informações a seguir apresentam as constantes e os tipos de dados necessários a serem usados para esse conjunto de propriedades em chamadas para métodos [**IKsPropertySet**](ikspropertyset.md) . Ele fornece valores para os parâmetros **GUID** (*GUIDPROPSET*), ID de propriedade (*dwPropId*) e tipo de dados de propriedade (*pPropData*).



|                   |                           |
|-------------------|---------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ CopyProt |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>ID da propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></td>
<td>Consulta se a saída de vídeo é um vídeo de componente analógico e de definição padrão.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_COPY_MACROVISION</td>
<td>Esta é uma propriedade somente de conjunto. Essa propriedade define o nível de proteção de cópia analógica para o codificador NTSC na extremidade de saída do PIN de recebimento. Usa <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_CHLG_KEY</td>
<td>As operações Get e Set têm suporte nessa propriedade. Uma operação get solicita que o decodificador forneça sua chave de desafio de barramento. Uma operação de definição fornece o decodificador com a chave de desafio de barramento da unidade de DVD. Os dados passados nesta propriedade serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DEC_KEY2</td>
<td>Esta é uma propriedade somente obtenção. Essa propriedade solicita que a tecla de barramento 2 do decodificador seja transferida para a unidade de DVD. Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_DISC_KEY</td>
<td>Propriedade Set-only. Isso fornece a chave do disco. A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_DVD_KEY1</td>
<td>Esta é uma propriedade somente de conjunto. Essa propriedade fornece a chave 1 do barramento de unidade de DVD para o decodificador. Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_REGION</td>
<td>Código de região solicita a definição de região que o decodificador tem permissão para reproduzir, conforme definido pelo DVD Consortium. Essa região é definida como uma estrutura de <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> .</td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_SET_COPY_STATE</td>
<td>Tanto Get quanto Set têm suporte nessa propriedade. Get é chamado primeiro para determinar se a autenticação é necessária. As propriedades definidas são indicações sobre qual fase da negociação de proteção de cópia o filtro está inserindo. Os dados passados serão uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</td>
<td>Se essa propriedade for <strong>true</strong>, o navegador de DVD não enviará amostras de <strong>AM_UseNewCSSKey</strong> antes de negociar a chave de disco. Consulte <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.<br/> Somente leitura. Os dados da propriedade são um valor <strong>bool</strong> .<br/>
<blockquote>
[!Note]<br />
Aplica-se ao Windows 7.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>AM_PROPERTY_DVDCOPY_TITLE_KEY</td>
<td>Esta é uma propriedade somente de conjunto. Isso fornece a chave de título do conteúdo atual. A chave é uma estrutura do tipo <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




