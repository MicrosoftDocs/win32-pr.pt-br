---
title: WINBIO_EVENT estrutura (Tipos \_ winbio.h)
description: Contém informações de status enviadas para a rotina de retorno de chamada quando um aviso de evento é gerado.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT estrutura Windows API do Biometric Framework
- PWINBIO_EVENT de estrutura Windows API do Biometric Framework
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
ms.openlocfilehash: 6e3baab16ee7c3f825f317d7aa2c585cb4d8ae7d6d030b6f59a1555b95343015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910539"
---
# <a name="winbio_event-structure"></a>Estrutura DE \_ EVENTO WINBIO

A **estrutura WINBIO \_ EVENT** contém informações de status enviadas para a rotina de retorno de chamada quando um aviso de evento é gerado.

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

Um valor que especifica o tipo de aviso de evento do provedor de serviços gerado. O único provedor atualmente com suporte é o sensor de impressão digital. Esse sensor dá suporte aos sinalizadores a seguir.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED** (o sensor detectou um dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco. O Windows Biometric Framework chama em sua função de retorno de chamada para indicar que ocorreu um deslizar o dedo, mas não tenta identificar a impressão digital.)
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED \_ IDENTIFY** (o sensor detectou um dedo que não foi solicitado pelo aplicativo ou pela janela que atualmente tem foco. O Windows Biometric Framework tenta identificar a impressão digital e passa o resultado desse processo para sua função de retorno de chamada.)
</dt> </dl> </dd> <dt>

**Parâmetros**
</dt> <dd> <dl> <dt>

**Unclaimed**
</dt> <dd>

Estrutura retornada para captura de amostra biométrica.

<dl> <dt>

**UnitId**
</dt> <dd>

A unidade biométrica que gerou o exemplo.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Um **valor ULONG** que contém informações adicionais sobre falha ao capturar uma amostra biométrica. Se uma captura for bem-sucedida, esse parâmetro será definido como zero. Os seguintes valores são definidos para captura de impressão digital:

-   WINBIO \_ FP \_ MUITO \_ ALTO
-   WINBIO \_ FP \_ MUITO \_ BAIXO
-   WINBIO \_ FP \_ MUITO À \_ ESQUERDA
-   WINBIO \_ FP \_ MUITO À \_ DIREITA
-   WINBIO \_ FP \_ TOO \_ FAST
-   WINBIO \_ FP \_ MUITO \_ LENTO
-   QUALIDADE RUIM \_ DO WINBIO FP \_ \_
-   WINBIO \_ FP \_ MUITO \_ DISTORCEDO
-   WINBIO \_ FP \_ MUITO \_ CURTO
-   FALHA DE MESCLAGEM DO WINBIO \_ FP \_ \_

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Estrutura retornada para captura biométrica e identificação. A identificação determina se uma amostra pode ser associada a um modelo biométrico existente.

<dl> <dt>

**UnitId**
</dt> <dd>

A unidade biométrica que gerou o exemplo.

</dd> <dt>

**Identidade**
</dt> <dd>

Uma [**estrutura WINBIO \_ IDENTITY**](winbio-identity.md) que contém o GUID ou SID do usuário que fornece a amostra biométrica.

</dd> <dt>

**Subfactor**
</dt> <dd>

Um [**valor DE \_ SUBTIPO BIOMÉTRICO \_ WINBIO**](winbio-biometric-subtype-constants.md) que especifica o sub-fator associado a uma amostra biométrica. Atualmente, Windows WBF (Biometric Framework) dá suporte apenas à captura de impressão digital e usa as constantes a seguir para representar informações de subtipo.

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
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ FOUR \_ FINGERS
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> Não tente validar o valor fornecido para o *valor SubFactor.* O Windows Biometria do serviço validará o valor fornecido antes de passá-lo para sua implementação. Se o valor for **WINBIO \_ SUBTYPE \_ NO INFORMATION \_ ou** **WINBIO \_ SUBTYPE \_ ANY**, valide quando apropriado.

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Um **valor ULONG** que contém informações adicionais sobre a falha ao capturar uma amostra biométrica. Se a captura for bem-sucedida, esse parâmetro será definido como zero. Os seguintes valores são definidos para captura de impressão digital:

-   WINBIO \_ FP \_ MUITO \_ ALTO
-   WINBIO \_ FP \_ MUITO \_ BAIXO
-   WINBIO \_ FP \_ MUITO À \_ ESQUERDA
-   WINBIO \_ FP \_ MUITO À \_ DIREITA
-   WINBIO \_ FP \_ TOO \_ FAST
-   WINBIO \_ FP \_ MUITO \_ LENTO
-   QUALIDADE RUIM \_ DO WINBIO FP \_ \_
-   WINBIO \_ FP \_ MUITO \_ DISTORCEDO
-   WINBIO \_ FP \_ MUITO \_ CURTO
-   FALHA DE MESCLAGEM DO WINBIO \_ FP \_ \_

</dd> </dl> </dd> <dt>

**Erro**
</dt> <dd>

Estrutura que identifica o êxito ou a falha da operação que está sendo monitorada.

<dl> <dt>

**ErrorCode**
</dt> <dd>

**Valor HRESULT** que contém S OK ou um código de erro que resultou de \_ cálculos executados pelo Windows Biometric Framework.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Chame a [**função WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) para registrar uma rotina de retorno de chamada para receber notificações de eventos do Windows Biometric Framework. O retorno de chamada é uma função personalizada que você deve definir para seu aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





