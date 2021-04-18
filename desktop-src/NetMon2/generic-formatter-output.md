---
description: As listas e tabelas nesta seção mostram a saída do formatador genérico. Lembre-se de que o formatador genérico usa os membros DataType e dataqualifier da estrutura PROPERTYINFO para determinar como formatar os dados exibidos.
ms.assetid: cf3dc6cd-7b24-464a-9d2b-5e35c4e8825e
title: Saída de formatador genérico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf4b334dd717c7ff332c3b730afb57d4be611ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759189"
---
# <a name="generic-formatter-output"></a>Saída de formatador genérico

As listas e tabelas nesta seção mostram a saída do [*formatador genérico*](g.md). Lembre-se de que o formatador genérico usa os membros **DataType** e **dataqualifier** da estrutura [**PROPERTYINFO**](propertyinfo.md) para determinar como formatar os dados exibidos.

Para obter mais informações e um exemplo da saída para um tipo de dados de propriedade específico, consulte:

-   [tipo de PROP \_ \_ void](/windows)
-   [\_Resumo do tipo prop \_](/windows)
-   [\_byte do tipo prop \_](/windows)
-   [tipo de PROP \_ \_ Word](/windows)
-   [tipo de PROP \_ \_ DWORD](/windows)
-   \_Tipo \_ de prop LARGEINT (formatador genérico não suporta)
-   \_ \_ Endereço de tipo de prop (formatador genérico não suporta)
-   [\_hora do tipo de prop \_](/windows)
-   [Cadeia de caracteres do \_ tipo prop \_](/windows)
-   [\_ \_ endereço IP do tipo prop \_](/windows)
-   PROP \_ Type \_ BYTESWAPPED \_ Word (obsoleto. Para obter mais informações, consulte [prop \_ Type \_ Word](/windows))
-   PROP \_ Type \_ BYTESWAPPED \_ DWORD (obsoleto. Para obter mais informações, consulte [prop \_ Type \_ DWORD](/windows))
-   \_ \_ \_ Cadeia de caracteres tipada do tipo prop (obsoleto)
-   [\_ \_ dados brutos do tipo prop \_](/windows)
-   [\_Comentário do tipo prop \_](/windows)
-   \_Tipo \_ de prop SRCFRIENDLYNAME (formatador genérico não suporta)
-   \_Tipo \_ de prop DSTFRIENDLYNAME (formatador genérico não suporta)
-   \_ \_ Endereço TOKENRING do tipo prop \_ (formatador genérico não suporta)
-   \_Tipo \_ de prop \_ endereço FDDI (formatador genérico não suporta)
-   \_ \_ Endereço Ethernet do tipo prop \_ (formatador genérico não suporta)
-   \_ \_ \_ Identificador de objeto do tipo prop (formatador genérico não suporta)
-   \_ \_ \_ Endereço IP de Vines do tipo prop \_ (formatador genérico não suporta)
-   Tipo de PROP \_ \_ var \_ Len \_ pequeno \_ int (formatador genérico não suporta)

## <a name="prop_type_void-and-prop_type_comment"></a>\_Tipo \_ de prop comentário de \_ tipo nulo e prop \_

A tabela a seguir lista a saída de formato genérico para propriedades do tipo de **prop \_ Type \_ void** e **prop \_ Type \_** de tipo de dados.

Na coluna saída do formatador, o valor dos dados na captura é XYZ.



| Qualificador de propriedade            | Saída do formatador                                      |
|-------------------------------|-------------------------------------------------------|
| PROP \_ igual \_ None              | XYZ                                                   |
| \_intervalo de igual prop \_             | XYZ                                                   |
| campo de igual de PROP \_ \_          | Obsoleto                                              |
| PROP \_ igual \_ rotulado \_ conjunto      | XYZ                                                   |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags |
| \_igual \_ const de prop             | XYZ                                                   |
| \_sinalizadores de igual de prop \_             | XYZ                                                   |
| \_matriz igual \_ prop             | XYZ                                                   |



 

## <a name="prop_type_summary"></a>\_Resumo do tipo prop \_

A tabela a seguir lista a saída de formato genérico para propriedades de tipo de dados de **\_ \_ Resumo do tipo prop** .

Na coluna saída de exemplo, o valor dos dados na captura é XYZ.



| Qualificador de propriedade            | Saída de exemplo                                        |
|-------------------------------|-------------------------------------------------------|
| PROP \_ igual \_ None              | XYZ                                                   |
| \_intervalo de igual prop \_             | XYZ                                                   |
| campo de igual de PROP \_ \_          | Obsoleto                                              |
| PROP \_ igual \_ rotulado \_ conjunto      | XYZ                                                   |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags |
| \_igual \_ const de prop             | XYZ                                                   |
| \_sinalizadores de igual de prop \_             | XYZ                                                   |
| \_matriz igual \_ prop             | XYZ                                                   |



 

## <a name="prop_type_byte"></a>\_byte do tipo prop \_

A tabela a seguir lista a saída de formato genérico para propriedades de tipo de dados de **\_ \_ tipo de prop** .

Na coluna saída de exemplo, o valor dos dados na captura é 10.



| Qualificador de propriedade            | Saída de exemplo                                                                                                |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| PROP \_ igual \_ None              | 10 (0xA) "                                                                                                     |
| \_intervalo de igual prop \_             | 10 (0xA) intervalo:(1 (0x1)-20 (0x14))                                                                          |
| \_conjunto de igual prop \_               | 10 (0xA) corresponde ao valor definido ou<br/> 10 (0xA) valor de conjunto desconhecido<br/>                                |
| campo de igual de PROP \_ \_          | Obsoleto.                                                                                                     |
| PROP \_ igual \_ rotulado \_ conjunto      | Rótulo correspondente em um conjunto de rótulos ou número.                                                                 |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags.                                                        |
| \_igual \_ const de prop             | Nenhuma saída. Nenhum dado é exibido no painel de detalhes.                                                           |
| \_sinalizadores de igual de prop \_             | ....... 0 = rótulo off cadeia de caracteres...... uma. = Rótulo na cadeia de caracteres..... 0.. = Rótulo off cadeia de caracteres... 1... = rótulo na cadeia de caracteres |
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
| campo de igual de PROP \_ \_          | Obsoleto.                                                   |
| PROP \_ igual \_ rotulado \_ conjunto      | Exibe a hora do sistema com base no relógio do computador local. |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags.      |
| \_igual \_ const de prop             | Exibe a hora do sistema com base no relógio do computador local. |
| \_sinalizadores de igual de prop \_             | Exibe a hora do sistema com base no relógio do computador local. |
| \_matriz igual \_ prop             | Exibe a hora do sistema com base no relógio do computador local. |



 

## <a name="prop_type_string"></a>Cadeia de caracteres do \_ tipo prop \_

A tabela a seguir lista a saída de formato genérico para propriedades de tipo de dados de **\_ cadeia de \_ caracteres de tipo prop** . Lembre-se de que a saída do formatador pode variar dependendo do qualificador de dados da propriedade.



| Qualificador de propriedade            | Saída do formatador                                       |
|-------------------------------|--------------------------------------------------------|
| PROP \_ igual \_ None              | Cadeia de caracteres anexada.                                       |
| \_intervalo de igual prop \_             | Cadeia de caracteres anexada.                                       |
| campo de igual de PROP \_ \_          | Obsoleto.                                              |
| PROP \_ igual \_ rotulado \_ conjunto      | Cadeia de caracteres anexada.                                       |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags. |
| \_igual \_ const de prop             | Cadeia de caracteres anexada.                                       |
| \_sinalizadores de igual de prop \_             | Cadeia de caracteres anexada.                                       |
| \_matriz igual \_ prop             | Cadeia de caracteres anexada.                                       |



 

## <a name="prop_type_ip_address"></a>\_ \_ endereço IP do tipo prop \_

A tabela a seguir lista a saída de formato genérico para o tipo de prop Propriedades de tipo de dados de **\_ \_ \_ endereço IP** . Lembre-se de que a saída formatada pode variar dependendo do qualificador de dados de propriedade da propriedade.

Na coluna saída de exemplo, o valor dos dados na captura é "129.65.100.2".



| Qualificador de propriedade            | Saída de exemplo                                         |
|-------------------------------|--------------------------------------------------------|
| PROP \_ igual \_ None              | 129.65.100.2                                           |
| \_intervalo de igual prop \_             | 129.65.100.2                                           |
| campo de igual de PROP \_ \_          | Obsoleto.                                              |
| PROP \_ igual \_ rotulado \_ conjunto      | 129.65.100.2                                           |
| PROP \_ igual \_ rotulado como campo de bits \_ | Obsoleto. Para obter mais informações, consulte PROP \_ igual \_ flags. |
| \_igual \_ const de prop             | 129.65.100.2                                           |
| \_sinalizadores de igual de prop \_             | 129.65.100.2                                           |
| \_matriz igual \_ prop             | 129.65.100.2                                           |



 

 

