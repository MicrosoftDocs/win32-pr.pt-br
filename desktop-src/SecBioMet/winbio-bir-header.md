---
title: Estrutura de WINBIO_BIR_HEADER (WinBio \_ Types. h)
description: Contém o cabeçalho de um BIR (registro de informações biométricas).
ms.assetid: 4b020720-42ef-4ac7-aaa3-7a0e45198890
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BIR_HEADER
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
ms.openlocfilehash: 1479c0db3ee826d79cf95a311215c8cf76f1c96b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085562"
---
# <a name="winbio_bir_header-structure"></a>\_Estrutura de \_ cabeçalho WINBIO Bir

A estrutura de **\_ \_ cabeçalho WINBIO Bir** contém o cabeçalho de um Bir (registro de informações biométricas).

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

Bitmask que especifica quais campos nessa estrutura são válidos. Para obter mais informações, consulte [**WINBIO \_ Bir \_ Field Constants**](winbio-bir-field-constants.md).

</dd> <dt>

**HeaderVersion**
</dt> <dd>

Uma constante de **\_ \_ versão WINBIO Bir** que especifica a versão do cabeçalho. Os números de versão são valores de 8 bits em que os quatro bits superiores especificam o número principal e os quatro bits baixos especificam o número de versão secundária. Atualmente, ele deve ser \_ WINBIO \_ \_ (versão de cabeçalho CBEFF).

</dd> <dt>

**PatronHeaderVersion**
</dt> <dd>

Uma constante de **\_ \_ versão WINBIO Bir** que especifica a versão do cabeçalho. Os números de versão são valores de 8 bits em que os quatro bits superiores especificam o número principal e os quatro bits baixos especificam o número de versão secundária. Atualmente, ele deve ser \_ WINBIO \_ \_ (versão de cabeçalho Patron).

</dd> <dt>

**Sinalizadores de**
</dt> <dd>

Um valor que especifica o formato dos dados de cabeçalho. Isso pode ser uma **ou uma ou** mais das seguintes sinalizações de nível de segurança e de processamento. Para obter mais informações, [**consulte \_ constantes \_ de \_ sinalizadores de dados do WINBIO Bir**](winbio-bir-data-flags-constants.md).



| Valor                                                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_FLAG_PRIVACY"></span><span id="winbio_data_flag_privacy"></span><dl> <dt>**WINBIO \_ \_ \_ Privacidade do sinalizador de dados**</dt> <dt>((UCHAR) 0x02)</dt> </dl>                                       | Os dados estão criptografados.<br/>                                                                                                                                                                                   |
| <span id="WINBIO_DATA_FLAG_INTEGRITY"></span><span id="winbio_data_flag_integrity"></span><dl> <dt>**WINBIO \_ \_ \_ Integridade do sinalizador de dados**</dt> <dt>((UCHAR) 0x01)</dt> </dl>                                 | Os dados são assinados digitalmente ou protegidos por um MAC (código de autenticação de mensagem).<br/>                                                                                                                        |
| <span id="WINBIO_DATA_FLAG_SIGNED"></span><span id="winbio_data_flag_signed"></span><dl> <dt>**WINBIO \_ Sinalizador de dados \_ \_ assinado**</dt> <dt>((UCHAR) 0x04)</dt> </dl>                                          | Se esse sinalizador e o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** estiverem definidos, os dados serão assinados. Se esse sinalizador não for definido, mas o sinalizador de **\_ integridade do \_ sinalizador \_ de dados WINBIO** for definido, um Mac será calculado sobre os dados.<br/> |
| <span id="WINBIO_DATA_FLAG_RAW"></span><span id="winbio_data_flag_raw"></span><dl> <dt>**WINBIO \_ Sinalizador de dados \_ \_ RAW**</dt> <dt>((UCHAR) 0x20)</dt> </dl>                                                   | Os dados estão no formato com o qual foram capturados.<br/>                                                                                                                                                    |
| <span id="WINBIO_DATA_FLAG_INTERMEDIATE"></span><span id="winbio_data_flag_intermediate"></span><dl> <dt>**WINBIO \_ Sinalizador de dados \_ \_ intermediário**</dt> <dt>((UCHAR) 0x40)</dt> </dl>                        | Os dados não são brutos, mas não foram completamente processados.<br/>                                                                                                                                               |
| <span id="WINBIO_DATA_FLAG_PROCESSED"></span><span id="winbio_data_flag_processed"></span><dl> <dt>**WINBIO \_ Sinalizador de dados \_ \_ processado**</dt> <dt>((UCHAR) 0x80)</dt> </dl>                                 | Os dados foram processados.<br/>                                                                                                                                                                             |
| <span id="WINBIO_DATA_FLAG_OPTION_MASK_PRESENT"></span><span id="winbio_data_flag_option_mask_present"></span><dl> <dt>**WINBIO \_ Máscara de opção de sinalizador de dados \_ \_ \_ \_ presente**</dt> <dt>((UCHAR) 0x08)</dt> </dl> | Esse valor é sempre 1.<br/>                                                                                                                                                                                  |



 

</dd> <dt>

**Tipo**
</dt> <dd>

Um \_ \_ valor de tipo biométrico WINBIO que especifica o tipo de dados biométricos referenciados no registro de informações biométricas. Atualmente, somente a **\_ \_ impressão digital do tipo WINBIO** tem suporte. Para obter mais informações, [**consulte \_ constantes do \_ tipo biométrico WINBIO**](winbio-biometric-type-constants.md).

</dd> <dt>

**Subtipo**
</dt> <dd>

Um valor de **\_ \_ subtipo biométrico WINBIO** que especifica o subfator associado aos dados biométricos. Para obter mais informações, consulte [**constantes de \_ \_ subtipo de comentários e WINBIO biométricas**](winbio-biometric-subtype-constants.md).

</dd> <dt>

**Finalidade**
</dt> <dd>

Uma máscara de **\_ \_ finalidade WINBIO Bir** que especifica o uso pretendido dos dados. Isso pode ser um valor de bits **ou** um dos valores a seguir. Para obter mais informações, [**consulte \_ constantes de \_ finalidade do WINBIO Bir**](winbio-bir-purpose-constants.md).

-   \_verificação de finalidade do WINBIO \_
-   \_identificação de finalidade do WINBIO \_
-   \_registro de finalidade do WINBIO \_
-   \_ \_ registro de finalidade \_ do WINBIO para \_ verificação
-   \_ \_ registro de finalidade \_ do WINBIO para \_ identificação
-   \_auditoria de finalidade do WINBIO \_

</dd> <dt>

**Alta qualidade**
</dt> <dd>

Um valor que especifica a qualidade relativa dos dados biométricos no registro de informações biométricas (BIR). Isso pode ser um número inteiro de 0 a 100 ou um dos valores a seguir. Para obter mais informações, consulte [**WINBIO \_ Bir \_ Quality Constants**](winbio-bir-quality-constants.md).



| Valor                                                                                                                                                                                                                                                                                                        | Significado                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ Qualidade de dados \_ \_ não \_ definida**</dt> <dt>((WINBIO \_ Bir \_ Quality)-1)</dt> </dl>                   | As medições de qualidade têm suporte pelo criador BIR, mas nenhum valor é definido no BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ Qualidade de dados \_ \_ sem \_ suporte**</dt> <dt>((WINBIO \_ Bir \_ Quality)-2)</dt> </dl> | As medições de qualidade não são suportadas pelo criador do BIR.<br/>                            |



 

</dd> <dt>

**CreationDate**
</dt> <dd>

A data e a hora, em tempo universal coordenado (hora de Greenwich), que o BIR foi criado.

</dd> <dt>

**ValidityPeriod**
</dt> <dd>

O período para o qual o BIR é válido.

<dl> <dt>

**BeginDate**
</dt> <dd>

A data e a hora, no tempo universal coordenado, que o período de validade inicia.

</dd> <dt>

**Término**
</dt> <dd>

A data e a hora, no tempo universal coordenado, em que o BIR deixa de ser válido.

</dd> </dl> </dd> <dt>

**BiometricDataFormat**
</dt> <dd>

Uma estrutura de [**\_ \_ formato registrada WINBIO**](winbio-registered-format.md) que especifica o formato de dados do bloco de dados Standard na estrutura [**\_ Bir WINBIO**](winbio-bir.md) . Os membros do **\_ \_ formato registrado WINBIO** não podem ser zero. Você pode usar as constantes a seguir para simplificar a verificação de erros.



| Valor                                                                                                                                                                                                                                                                                      | Significado                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_NO_FORMAT_OWNER_AVAILABLE"></span><span id="winbio_no_format_owner_available"></span><dl> <dt>**WINBIO \_ NENHUM \_ proprietário de formato \_ \_ disponível**</dt> <dt>((UShort) 0)</dt> </dl> | Nenhum valor de proprietário atribuído de IBIA (Associação Internacional de setores biométricos) foi especificado.<br/> |
| <span id="WINBIO_NO_FORMAT_TYPE_AVAILABLE"></span><span id="winbio_no_format_type_available"></span><dl> <dt>**WINBIO \_ NENHUM \_ tipo de formato \_ \_ disponível**</dt> <dt>((UShort) 0)</dt> </dl>    | Nenhum tipo de formato foi especificado.<br/>                                                              |



 

</dd> <dt>

**ProductId**
</dt> <dd>

Uma estrutura de [**\_ \_ formato registrada WINBIO**](winbio-registered-format.md) que especifica a ID do produto do componente que gerou o bloco de dados Standard no Bir. Os membros do **\_ \_ formato registrado WINBIO** podem ser zero.

</dd> </dl>

## <a name="remarks"></a>Comentários

O parâmetro *subtipo* especifica o subfator associado aos dados biométricos. Atualmente, o Windows Biometric Framework (WBF) dá suporte apenas à captura de impressão digital e usa as seguintes constantes para representar informações de subtipo:

-   WINBIO \_ ANSI \_ 381 \_ pos \_ desconhecido
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ Thumb
-   Dedo do índice de RH do WINBIO \_ ANSI \_ 381 \_ pos \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ \_ meio-dedo central de RH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ - \_ anel de RH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos de \_ LH \_ Thumb
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ do \_ meio- \_ dedo médio
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Ring \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ com \_ quatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ dois \_ polegares

> [!IMPORTANT]
>
> Não tente validar o valor fornecido para o valor do parâmetro de *subtipo* . O serviço de biometria do Windows validará o valor fornecido antes de passá-lo para sua implementação. Se o valor for **WINBIO \_ subtipo \_ nenhuma \_ informação** ou **\_ subtipo WINBIO \_**, em seguida, valide quando apropriado.

 

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
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

 

 





