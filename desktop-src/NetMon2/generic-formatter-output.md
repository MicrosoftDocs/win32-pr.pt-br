---
description: As listas e tabelas nesta seção mostram a saída do formatante genérico. Esteja ciente de que o formatante genérico usa os membros DataType e DataQualifier da estrutura PROPERTYINFO para determinar como formatar os dados exibidos.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Saída de formatação genérica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d76a67fadbed3bde5eb3e5534c8f104e918ac870df27c767b98575058a0a188
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743966"
---
# <a name="generic-formatter-output"></a>Saída de formatação genérica

As listas e tabelas nesta seção mostram a saída do [*formatante genérico*](g.md). Esteja ciente de que o formatante genérico usa os membros **DataType** e **DataQualifier** da estrutura [**PROPERTYINFO**](propertyinfo.md) para determinar como formatar os dados exibidos.

Para obter mais informações e um exemplo da saída para um tipo de dados de propriedade específico, consulte:

-   [TIPO \_ DE PROP \_ VOID](/windows)
-   [RESUMO DO \_ TIPO \_ PROP](/windows)
-   [BYTE \_ DE TIPO \_ PROP](/windows)
-   [PALAVRA DE \_ TIPO \_ PROP](/windows)
-   [PROP \_ TYPE \_ DWORD](/windows)
-   PROP \_ TYPE \_ LARGEINT (não há suporte para formatação genérica)
-   ADDR \_ DE \_ TIPO PROP (o formatador genérico não dá suporte)
-   [HORA DO \_ TIPO \_ PROP](/windows)
-   [CADEIA DE \_ CARACTERES DE TIPO \_ PROP](/windows)
-   [ENDEREÇO \_ IP DO TIPO \_ \_ PROP](/windows)
-   PROP \_ TYPE \_ BYTESWAPPED \_ WORD (obsoleto. Para obter mais informações, consulte [PROP \_ TYPE \_ WORD](/windows))
-   TIPO DE PROP \_ \_ BYTESWAPPED \_ DWORD (obsoleto. Para obter mais informações, consulte [PROP \_ TYPE \_ DWORD](/windows))
-   PROP \_ TYPE \_ TYPED STRING \_ (obsoleto)
-   [DADOS \_ BRUTOS \_ DO TIPO \_ PROP](/windows)
-   [COMENTÁRIO \_ DE TIPO \_ PROP](/windows)
-   PROP \_ TYPE \_ SRCFRIENDLYNAME (não há suporte para formatação genérica)
-   PROP \_ TYPE \_ DSTFRIENDLYNAME (não há suporte para formatação genérica)
-   PROP \_ TYPE \_ TOKENRING ADDRESS \_ (formattter genérico não dá suporte)
-   PROP \_ TYPE \_ FDDI \_ ADDRESS (formattter genérico não dá suporte)
-   PROP \_ TYPE ETHERNET ADDRESS \_ \_ (formattter genérico não dá suporte)
-   IDENTIFICADOR DE OBJETO DE TIPO PROP (não há suporte \_ \_ para \_ formatador genérico)
-   PROP \_ TYPE \_ VINES IP ADDRESS \_ \_ (formattter genérico não dá suporte)
-   PROP \_ TYPE VAR LEN SMALL \_ \_ \_ \_ INT (formattter genérico não dá suporte)

## <a name="prop_type_void-and-prop_type_comment"></a>PROP \_ TYPE VOID e PROP TYPE \_ \_ \_ COMMENT

A tabela a seguir lista a saída de formato genérico para propriedades de tipo de dados **PROP \_ TYPE \_ VOID** e **PROP TYPE \_ \_ COMMENT.**

Na coluna de saída do formatante, o valor dos dados na captura é XYZ.



| Qualificador de propriedade            | Saída do formatante                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| INTERVALO DE \_ QUAL \_ PROP             | XYZ                                                   |
| PROP \_ QUAL \_ BITFIELD          | Obsoleto                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| PROP \_ QUAL \_ ROTULADO \_ BITFIELD | Obsoleto. Para obter mais informações, consulte PROP \_ QUAL \_ FLAGS |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| SINALIZADORES \_ PROP QUAL \_             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>RESUMO DO \_ TIPO \_ PROP

A tabela a seguir lista a saída de formato genérico para **propriedades de tipo de dados PROP TYPE \_ \_ SUMMARY.**

Na coluna de saída de exemplo, o valor dos dados na captura é XYZ.



| Qualificador de propriedade            | Saída de exemplo                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | XYZ                                                   |
| INTERVALO DE \_ QUAL \_ PROP             | XYZ                                                   |
| PROP \_ QUAL \_ BITFIELD          | Obsoleto                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | XYZ                                                   |
| PROP \_ QUAL \_ ROTULADO \_ BITFIELD | Obsoleto. Para obter mais informações, consulte PROP \_ QUAL \_ FLAGS |
| PROP \_ QUAL \_ CONST             | XYZ                                                   |
| SINALIZADORES \_ PROP QUAL \_             | XYZ                                                   |
| PROP \_ QUAL \_ ARRAY             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>BYTE \_ DE TIPO \_ PROP

A tabela a seguir lista a saída de formato genérico para propriedades de tipo de dados **\_ PROP TYPE \_ BYTE.**

Na coluna de saída de exemplo, o valor dos dados na captura é 10.



| Qualificador de propriedade            | Saída de exemplo                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 10 (0xa)"                                                                                                     |
| INTERVALO DE \_ QUAL \_ PROP             | 10 (0xa) Intervalo:(1 (0x1) – 20 (0x14))                                                                          |
| PROP \_ QUAL \_ SET               | 10 (0xa) Corresponde ao valor definido ou<br/> 10 (0xa) Valor de conjunto desconhecido<br/>                                |
| PROP \_ QUAL \_ BITFIELD          | Obsoleto.                                                                                                     |
| PROP \_ QUAL \_ LABELED \_ SET      | Rótulo correspondente em um conjunto de rótulos ou número.                                                                 |
| PROP \_ QUAL \_ ROTULADO \_ BITFIELD | Obsoleto. Para obter mais informações, consulte PROP \_ QUAL \_ FLAGS.                                                        |
| PROP \_ QUAL \_ CONST             | Nenhuma saída. Nenhum dado é exibido no painel de detalhes.                                                           |
| SINALIZADORES \_ PROP QUAL \_             | ....... 0 = Rotular a cadeia de caracteres ...... 1. = Rótulo na cadeia de caracteres..... 0.. = Rótulo off cadeia de caracteres... 1... = rótulo na cadeia de caracteres |
| \_matriz igual \_ prop             | 0A FF...                                                                                                     |



 

## <a name="prop_type_word"></a>tipo de PROP \_ \_ Word

A tabela a seguir lista a saída de formato genérico para um tipo de prop Propriedade tipo de dados do **\_ \_ Word** .

> [!Note]  
> Para propriedades DWORD não Intel, trocadas por bytes, você deve alterar os dados para um formato Intel. Para alterar o formato, defina o parâmetro *iFlags* da função de instância da propriedade **Attach** IFLAG \_ permutada ao mapear a instância de propriedade para um local.

 

Na coluna saída de exemplo, o valor dos dados na captura é 10.



| Qualificador de propriedade            | Saída de exemplo                                                                                                                                                                                                                |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ igual \_ None              | 10 (0xA)                                                                                                                                                                                                                      |
| \_intervalo de igual prop \_             | 10 (0xA) intervalo:(1 (0x1)-20 (0x14))                                                                                                                                                                                          |
| \_conjunto de igual prop \_               | 10 (0xA) corresponde ao valor definido ou<br/> 10 (0xA) valor de conjunto desconhecido<br/>                                                                                                                                                |
| campo de igual de PROP \_ \_          | Obsoleto.                                                                                                                                                                                                                     |
| PROP \_ igual \_ rotulado \_ conjunto      | Rótulo correspondente no conjunto de rótulos ou no número.                                                                                                                                                                               |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags.                                                                                                                                                                        |
| \_igual \_ const de prop             | Nenhuma saída. Nenhum dado é exibido no painel de detalhes.                                                                                                                                                                           |
| \_sinalizadores de igual de prop \_             | ....... 0 = rótulo off cadeia de caracteres...... 0. = Rótulo off cadeia de caracteres..... 0.. = Rótulo off cadeia de caracteres... 0... = rótulo off cadeia de caracteres... 0.... = rótulo off cadeia de caracteres.. 1.... = Rótulo na cadeia de caracteres. 0...... = Rótulo fora da cadeia de caracteres 1....... = Rótulo na cadeia de caracteres |
| \_matriz igual \_ prop             | 000A ffff...                                                                                                                                                                                                                 |



 

## <a name="prop_type_dword"></a>tipo de PROP \_ \_ DWORD

A tabela a seguir lista a saída de formato genérico para propriedades de tipo de dados **\_ \_ DWORD do tipo prop** .

> [!Note]  
> Para propriedades DWORD não Intel, trocadas por bytes, você deve alterar os dados para um formato Intel. Para alterar o formato, defina o parâmetro *iFlags* da função de instância da propriedade **Attach** IFLAG \_ permutada ao mapear a instância de propriedade para um local.

 

Na coluna saída de exemplo, o valor dos dados na captura é 10.



| Qualificador de propriedade            | Saída de exemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PROP \_ igual \_ None              | 10 (0xA)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| \_intervalo de igual prop \_             | 10 (0xA) intervalo:(1 (0x1)-20 (0x14))                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| \_conjunto de igual prop \_               | 10 (0xA) corresponde ao valor definido ou<br/> 10 (0xA) valor de conjunto desconhecido<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| campo de igual de PROP \_ \_          | Obsoleto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROP \_ igual \_ rotulado \_ conjunto      | Rótulo correspondente no conjunto de rótulos ou no número.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_igual \_ const de prop             | Nenhuma saída. Nenhum dado é exibido no painel de detalhes.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_sinalizadores de igual de prop \_             | ............... 0 = rótulo off cadeia de caracteres.................... 0. = Rótulo off cadeia de caracteres............... 0.. = Rótulo off cadeia de caracteres............ 0... = rótulo off cadeia de caracteres................. 0.... = rótulo off cadeia de caracteres................ 0.... = Rótulo off cadeia de caracteres......... 0...... = rótulo off cadeia de caracteres........ 0....... = rótulo off cadeia de caracteres....... 0........ = Rótulo off cadeia de caracteres...... 0......... = rótulo off cadeia de caracteres..... 0.......... = rótulo off cadeia de caracteres.... 0........... = Rótulo desativado cadeia de caracteres... 0............ = rótulo off cadeia de caracteres.. 1............ = rótulo na cadeia de caracteres. 0............. = Rótulo fora da cadeia de caracteres 1...................... = Rótulo na cadeia de caracteres |
| \_matriz igual \_ prop             | 0000000A ffffffff...                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="prop_type_raw_data"></a>\_ \_ dados brutos do tipo prop \_

A tabela a seguir lista a saída de formato genérico para uma propriedade de tipo de dados de **\_ \_ \_ dados brutos de tipo prop** . Lembre-se de que a saída do formatador não exibe os dados brutos, mas exibe o rótulo da propriedade.



| Qualificador de propriedade            | Saída do formatador |
|-------------------------------|------------------|
| PROP \_ igual \_ None              | Rótulo da propriedade.  |
| \_intervalo de igual prop \_             | Rótulo da propriedade.  |
| campo de igual de PROP \_ \_          | Rótulo da propriedade.  |
| PROP \_ igual \_ rotulado \_ conjunto      | Rótulo da propriedade.  |
| PROP \_ igual \_ rotulado como campo de bits \_ | Rótulo da propriedade.  |
| \_igual \_ const de prop             | Rótulo da propriedade.  |
| \_sinalizadores de igual de prop \_             | Rótulo da propriedade.  |
| \_matriz igual \_ prop             | Rótulo da propriedade.  |



 

## <a name="prop_type_time"></a>\_hora do tipo de prop \_

A tabela a seguir lista a saída de formato genérico para uma propriedade de tipo de dados **\_ \_ time de tipo prop** . Lembre-se de que a saída formatada pode variar dependendo do qualificador de dados da propriedade.

O formatador genérico chama [**GetDateFormat**](/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata) para obter um tempo baseado no relógio do sistema do computador local.



| Qualificador de propriedade            | Saída do formatador                                            |
|-------------------------------|-------------------------------------------------------------|
| PROP \_ igual \_ None              | Exibe a hora do sistema com base no relógio do computador local. |
| \_intervalo de igual prop \_             | Exibe a hora do sistema com base no relógio do computador local. |
| PROP \_ QUAL \_ BITFIELD          | Obsoleto.                                                   |
| PROP \_ QUAL \_ LABELED \_ SET      | Exibe a hora do sistema com base no relógio do computador local. |
| PROP \_ QUAL \_ ROTULADO \_ BITFIELD | Obsoleto. Para obter mais informações, consulte PROP \_ QUAL \_ FLAGS.      |
| PROP \_ QUAL \_ CONST             | Exibe a hora do sistema com base no relógio do computador local. |
| SINALIZADORES \_ PROP QUAL \_             | Exibe a hora do sistema com base no relógio do computador local. |
| PROP \_ QUAL \_ ARRAY             | Exibe a hora do sistema com base no relógio do computador local. |



 

## <a name="prop_type_string"></a>CADEIA DE \_ CARACTERES DE TIPO \_ PROP

A tabela a seguir lista a saída de formato genérico para propriedades **de tipo de dados PROP TYPE \_ \_ STRING.** Esteja ciente de que a saída do formatador pode variar dependendo do qualificador de dados da propriedade.



| Qualificador de propriedade            | Saída do formatante                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | Cadeia de caracteres anexada.                                       |
| INTERVALO DE \_ QUAL \_ PROP             | Cadeia de caracteres anexada.                                       |
| PROP \_ QUAL \_ BITFIELD          | Obsoleto.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | Cadeia de caracteres anexada.                                       |
| PROP \_ QUAL \_ ROTULADO \_ BITFIELD | Obsoleto. Para obter mais informações, consulte PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | Cadeia de caracteres anexada.                                       |
| SINALIZADORES \_ PROP QUAL \_             | Cadeia de caracteres anexada.                                       |
| PROP \_ QUAL \_ ARRAY             | Cadeia de caracteres anexada.                                       |



 

## <a name="prop_type_ip_address"></a>ENDEREÇO \_ IP DO TIPO \_ \_ PROP

A tabela a seguir lista a saída de formato genérico para propriedades de tipo de dados **\_ ENDEREÇO IP \_ \_ DO** TIPO PROP. Esteja ciente de que a saída formatada pode variar dependendo do qualificador de dados de propriedade da propriedade.

Na coluna de saída de exemplo, o valor dos dados na captura é "129.65.100.2".



| Qualificador de propriedade            | Saída de exemplo                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ QUAL \_ NONE              | 129.65.100.2                                           |
| INTERVALO DE \_ QUAL \_ PROP             | 129.65.100.2                                           |
| PROP \_ QUAL \_ BITFIELD          | Obsoleto.                                              |
| PROP \_ QUAL \_ LABELED \_ SET      | 129.65.100.2                                           |
| PROP \_ QUAL \_ ROTULADO \_ BITFIELD | Obsoleto. Para obter mais informações, consulte PROP \_ QUAL \_ FLAGS. |
| PROP \_ QUAL \_ CONST             | 129.65.100.2                                           |
| SINALIZADORES \_ PROP QUAL \_             | 129.65.100.2                                           |
| PROP \_ QUAL \_ ARRAY             | 129.65.100.2                                           |



 

 

