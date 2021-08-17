---
title: WINBIO_BIR_HEADER estrutura (Tipos \_ winbio.h)
description: Contém o header de um BIR (registro de informações biométricos).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- WINBIO_BIR_HEADER estrutura Windows API do Biometric Framework
topic_type:
- apiref
api_name:
- WINBIO_BIR_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2166a206dd1590f83e16bc67482d3b42e24717efae4c44e54a99b9aa7d83b84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911079"
---
# <a name="winbio_bir_header-structure"></a>Estrutura WINBIO \_ BIR \_ HEADER

A **estrutura WINBIO \_ BIR \_ HEADER** contém o título de um BIR (registro de informações biométricos).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_BIR_HEADER {
  USHORT                   ValidFields;
  WINBIO_BIR_VERSION       HeaderVersion;
  WINBIO_BIR_VERSION       PatronHeaderVersion;
  WINBIO_BIR_DATA_FLAGS    DataFlags;
  WINBIO_BIOMETRIC_TYPE    Type;
  WINBIO_BIOMETRIC_SUBTYPE Subtype;
  WINBIO_BIR_PURPOSE       Purpose;
  WINBIO_BIR_QUALITY       DataQuality;
  LARGE_INTEGER            CreationDate;
  struct {
    LARGE_INTEGER BeginDate;
    LARGE_INTEGER EndDate;
  } ValidityPeriod;
  WINBIO_REGISTERED_FORMAT BiometricDataFormat;
  WINBIO_REGISTERED_FORMAT ProductId;
} WINBIO_BIR_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**ValidFields**
</dt> <dd>

Bitmask que especifica quais campos nesta estrutura são válidos. Para obter mais informações, consulte [**\_ \_ Constantes WINBIO BIR FIELD**](winbio-bir-field-constants.md).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Uma **constante \_ WINBIO BIR \_ VERSION** que especifica a versão do título. Os números de versão são valores de 8 bits em que os quatro bits superiores especificam o número principal e os quatro bits baixos especificam o número de versão secundária. Atualmente, isso deve ser WINBIO \_ CBEFF \_ HEADER \_ VERSION (0x11).

</dd> <dt>

**HeadheaderVersion**
</dt> <dd>

Uma **constante \_ WINBIO BIR \_ VERSION** que especifica a versão do título. Os números de versão são valores de 8 bits em que os quatro bits superiores especificam o número principal e os quatro bits baixos especificam o número de versão secundária. Atualmente, isso deve ser WINBIO \_ LTD \_ HEADER \_ VERSION (0x11).

</dd> <dt>

**DataFlags**
</dt> <dd>

Um valor que especifica o formato dos dados de header. Isso pode ser um OR bit a **bit** dos seguintes sinalizadores de nível de segurança e processamento. Para obter mais informações, consulte [**\_ Constantes DE SINALIZADORES DE DADOS BIR \_ \_ WINBIO**](winbio-bir-data-flags-constants.md).



| Valor                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ PRIVACIDADE \_ DO \_ SINALIZADOR DE**</dt> DADOS <dt>((UCHAR)0x02)</dt> </dl>                                       | Os dados estão criptografados.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ INTEGRIDADE \_ DO \_ SINALIZADOR DE**</dt> DADOS <dt>((UCHAR)0x01)</dt> </dl>                                 | Os dados são assinados digitalmente ou protegidos por um MAC (código de autenticação de mensagem).<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ SINALIZADOR \_ DE \_ DADOS ASSINADO**</dt> <dt>((UCHAR)0x04)</dt> </dl>                                          | Se esse sinalizador e o sinalizador INTEGRIDADE DO SINALIZADOR **DE DADOS WINBIO \_ \_ \_** estão definidos, os dados são assinados. Se esse sinalizador não estiver definido, mas o sinalizador INTEGRIDADE DO SINALIZADOR DE **\_ DADOS \_ \_ WINBIO** estiver definido, um MAC será calculado sobre os dados.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ RAW**</dt> <dt>((UCHAR)0x20)</dt> </dl>                                                   | Os dados estão no formato com o qual foram capturados.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ DATA \_ FLAG \_ INTERMEDIATE**</dt> <dt>((UCHAR)0x40)</dt> </dl>                        | Os dados não são brutos, mas não foram completamente processados.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ SINALIZADOR \_ DE \_ DADOS PROCESSADO**</dt> <dt>((UCHAR)0x80)</dt> </dl>                                 | Os dados foram processados.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ MÁSCARA DE \_ OPÇÃO DO SINALIZADOR DE DADOS \_ \_ \_ PRESENTE**</dt> <dt>((UCHAR)0x08)</dt> </dl> | Esse valor é sempre 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Tipo**
</dt> <dd>

Um valor DE \_ TIPO \_ BIOMÉTRICO WINBIO que especifica o tipo de dados biométricos referenciados no registro de informações biométricas. Atualmente, há suporte **apenas para WINBIO \_ TYPE \_ FINGERPRINT.** Para obter mais informações, consulte [**\_ \_ Constantes WINBIO BIOMETRIC TYPE**](winbio-biometric-type-constants.md).

</dd> <dt>

**Subtipo**
</dt> <dd>

Um **valor DE \_ SUBTIPO BIOMÉTRICO \_ WINBIO** que especifica o sub-fator associado aos dados biométricos. Para obter mais informações, consulte Comentários e Constantes [**\_ DE \_ SUBTIPO BIOMÉTRICO WINBIO**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Finalidade**
</dt> <dd>

Uma **máscara WINBIO \_ BIR \_ PURPOSE** que especifica o uso pretendido dos dados. Isso pode ser um **OR bit** a bit dos valores a seguir. Para obter mais informações, consulte [**\_ \_ Constantes WINBIO BIR PURPOSE**](winbio-bir-purpose-constants.md).

-   VERIFICAÇÃO DE \_ FINALIDADE DO \_ WINBIO
-   IDENTIFICAÇÃO DA \_ FINALIDADE DO WINBIO \_
-   REGISTRO DE FINALIDADE DO WINBIO \_ \_
-   REGISTRO DE FINALIDADE DO WINBIO \_ \_ PARA \_ \_ VERIFICAÇÃO
-   REGISTRO DE FINALIDADE DO WINBIO \_ \_ PARA \_ \_ IDENTIFICAÇÃO
-   AUDITORIA DE FINALIDADE DO WINBIO \_ \_

</dd> <dt>

**Igualdade de dados**
</dt> <dd>

Um valor que especifica a qualidade relativa dos dados biométricos no BIR (registro de informações biométricas). Pode ser um inteiro de 0 a 100 ou um dos valores a seguir. Para obter mais informações, consulte [**\_ \_ Constantes WINBIO BIR QUALITY**](winbio-bir-quality-constants.md).



| Valor                                                                                                                                                                                                                                                                                                        | Significado                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ QUALIDADE \_ DE DADOS NÃO \_ \_ DEFINIDA**</dt> <dt>((WINBIO \_ BIR \_ QUALITY)-1)</dt> </dl>                   | As medidas de qualidade são suportadas pelo criador do BIR, mas nenhum valor é definido no BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ QUALIDADE \_ DE DADOS SEM \_ \_ SUPORTE**</dt> <dt>((WINBIO \_ BIR \_ QUALITY)-2)</dt> </dl> | Não há suporte para medidas de qualidade pelo criador do BIR.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

A data e hora, em Tempo Universal Coordenado (Hora de Greenwich), em que o BIR foi criado.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

O período para o qual o BIR é válido.

<dl> <dt>

**BeginDate**
</dt> <dd>

A data e hora, em Tempo Universal Coordenado, que o período de validade é iniciado.

</dd> <dt>

**EndDate**
</dt> <dd>

A data e a hora, Tempo Universal Coordenado, na qual o BIR deixa de ser válido.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Uma [**estrutura WINBIO \_ REGISTERED \_ FORMAT**](winbio-registered-format.md) que especifica o formato de dados do bloco de dados padrão na [**estrutura \_ WINBIO BIR.**](winbio-bir.md) Os **membros WINBIO \_ REGISTERED \_ FORMAT** não podem ser zero. Você pode usar as constantes a seguir para simplificar a verificação de erros.



| Valor                                                                                                                                                                                                                                                                                      | Significado                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ SEM \_ PROPRIETÁRIO DE FORMATO \_ \_ DISPONÍVEL**</dt> <dt>((USHORT)0)</dt> </dl> | Nenhum valor de proprietário atribuído à IBIA (Associação Internacional do Setor Biométrico) foi especificado.<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ NENHUM \_ TIPO DE FORMATO \_ \_ DISPONÍVEL**</dt> <dt>((USHORT)0)</dt> </dl>    | Nenhum tipo de formato foi especificado.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Uma [**estrutura WINBIO \_ REGISTERED \_ FORMAT**](winbio-registered-format.md) que especifica a ID do produto do componente que gerou o bloco de dados padrão no BIR. Os **membros WINBIO \_ REGISTERED \_ FORMAT** podem ser zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

O *parâmetro Subtype* especifica o sub-fator associado aos dados biométricos. Atualmente, o WBF (Windows Biometric Framework) dá suporte apenas à captura de impressão digital e usa as seguintes constantes para representar informações de subtipo:

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ com \_ quatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ dois \_ polegares

> [!IMPORTANT]
>
> Não tente validar o valor fornecido para o valor do parâmetro de *subtipo* . o serviço de biometria Windows validará o valor fornecido antes de passá-lo para sua implementação. Se o valor for **WINBIO \_ subtipo \_ nenhuma \_ informação** ou **\_ subtipo WINBIO \_**, em seguida, valide quando apropriado.

 

Se qualquer um dos seguintes bits for declarado, a estrutura **de \_ \_ cabeçalho WINBIO Bir** não será corretamente formada.


```C++
#define WINBIO_BIR_FIELD_NEVER_VALID    (WINBIO_BIR_FIELD_SUBHEAD_COUNT |   \
                                         WINBIO_BIR_FIELD_PATRON_ID |       \
                                         WINBIO_BIR_FIELD_INDEX |           \
                                         WINBIO_BIR_FIELD_CHALLENGE |       \
                                         WINBIO_BIR_FIELD_PAYLOAD )
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**\_Constantes de SUBtipo de biometria WINBIO \_**](winbio-biometric-subtype-constants.md)
</dt> <dt>

[**WINBIO \_ Bir**](winbio-bir.md)
</dt> <dt>

[**\_Constantes de \_ sinalizadores de dados WINBIO Bir \_**](winbio-bir-data-flags-constants.md)
</dt> <dt>

[**\_Constantes do \_ campo WINBIO Bir**](winbio-bir-field-constants.md)
</dt> <dt>

[**Constantes de finalidade de \_ Bir WINBIO \_**](winbio-bir-purpose-constants.md)
</dt> <dt>

[**WINBIO \_ \_ constantes de qualidade Bir**](winbio-bir-quality-constants.md)
</dt> <dt>

[**\_Constantes da \_ versão WINBIO Bir**](winbio-bir-version-constants.md)
</dt> </dl>

 

 





