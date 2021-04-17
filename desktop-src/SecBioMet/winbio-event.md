---
title: Estrutura de WINBIO_EVENT (WinBio \_ Types. h)
description: Contém informações de status enviadas à rotina de retorno de chamada quando um aviso de evento é gerado.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EVENT
- Ponteiro de estrutura de PWINBIO_EVENT Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754611"
---
# <a name="winbio_event-structure"></a>\_Estrutura de eventos WINBIO

A estrutura de **\_ eventos WINBIO** contém informações de status enviadas à rotina de retorno de chamada quando um aviso de evento é gerado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo**
</dt> <dd>

Um valor que especifica o tipo de aviso de evento do provedor de serviço gerado. O único provedor com suporte no momento é o sensor de impressão digital. Este sensor dá suporte aos sinalizadores a seguir.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENTO \_ FP não \_ reivindicado** (o sensor detectou um dedo de dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco. O Windows Biometric Framework chama sua função de retorno de chamada para indicar que um dedo dedo ocorreu, mas não tenta identificar a impressão digital.)
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ \_Identificação de FP não \_ reivindicada \_ do evento** (o sensor detectou um dedo dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco. O Windows Biometric Framework tenta identificar a impressão digital e passa o resultado desse processo para sua função de retorno de chamada.)
</dt> </dl> </dd> <dt>

**Parâmetros**
</dt> <dd> <dl> <dt>

**Não reclamado**
</dt> <dd>

Estrutura retornada para captura de exemplo biométrica.

<dl> <dt>

**Unidadeid**
</dt> <dd>

A unidade biométrica que gerou o exemplo.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Um valor **ULONG** que contém informações adicionais sobre a falha ao capturar um exemplo biométrico. Se uma captura tiver sido bem-sucedida, esse parâmetro será definido como zero. Os seguintes valores são definidos para captura de impressão digital:

-   \_FP WINBIO \_ muito \_ alto
-   \_FP WINBIO \_ muito \_ baixo
-   \_FP WINBIO \_ muito \_ à esquerda
-   \_FP WINBIO \_ muito \_ à direita
-   \_FP WINBIO \_ muito \_ rápido
-   \_FP WINBIO \_ muito \_ lento
-   \_ \_ qualidade ruim de FP WINBIO \_
-   \_FP WINBIO \_ muito \_ distorcido
-   \_FP WINBIO \_ muito \_ curto
-   \_ \_ falha na mesclagem de FP WINBIO \_

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Estrutura retornada para captura e identificação biométricas. A identificação determina se um exemplo pode ser associado a um modelo biométrico existente.

<dl> <dt>

**Unidadeid**
</dt> <dd>

A unidade biométrica que gerou o exemplo.

</dd> <dt>

**Identidade**
</dt> <dd>

Uma estrutura de [**\_ identidade WINBIO**](winbio-identity.md) que contém o GUID ou o SID do usuário que fornece o exemplo biométrico.

</dd> <dt>

**Subfator**
</dt> <dd>

Um valor de [**\_ \_ subtipo biométrico WINBIO**](winbio-biometric-subtype-constants.md) que especifica o subfator associado a um exemplo biométrico. O Windows Biometric Framework (WBF) atualmente dá suporte apenas à captura de impressão digital e usa as constantes a seguir para representar informações de subtipo.

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
> Não tente validar o valor fornecido para o valor de *subfator* . O serviço de biometria do Windows validará o valor fornecido antes de passá-lo para sua implementação. Se o valor for **WINBIO \_ subtipo \_ nenhuma \_ informação** ou **\_ subtipo WINBIO \_**, em seguida, valide quando apropriado.

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Um valor **ULONG** que contém informações adicionais sobre a falha ao capturar um exemplo biométrico. Se a captura tiver sido bem-sucedida, esse parâmetro será definido como zero. Os seguintes valores são definidos para captura de impressão digital:

-   \_FP WINBIO \_ muito \_ alto
-   \_FP WINBIO \_ muito \_ baixo
-   \_FP WINBIO \_ muito \_ à esquerda
-   \_FP WINBIO \_ muito \_ à direita
-   \_FP WINBIO \_ muito \_ rápido
-   \_FP WINBIO \_ muito \_ lento
-   \_ \_ qualidade ruim de FP WINBIO \_
-   \_FP WINBIO \_ muito \_ distorcido
-   \_FP WINBIO \_ muito \_ curto
-   \_ \_ falha na mesclagem de FP WINBIO \_

</dd> </dl> </dd> <dt>

**Erro**
</dt> <dd>

Estrutura que identifica o êxito ou a falha da operação que está sendo monitorada.

<dl> <dt>

**ErrorCode**
</dt> <dd>

Valor **HRESULT** que contém S \_ OK ou um código de erro que resultou de computações executadas pelo Windows Biometric Framework.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Chame a função [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para registrar uma rotina de retorno de chamada para receber notificações de eventos da Windows Biometric Framework. O retorno de chamada é uma função personalizada que você deve definir para seu aplicativo.

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

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





