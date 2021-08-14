---
title: Estrutura de WINBIO_EXTENDED_ENROLLMENT_STATUS (WinBio \_ Types. h)
description: Contém informações adicionais sobre o status de um registro em andamento.
ms.assetid: 2FDDF4D3-6A3E-4DF5-ACA4-423F893C6F2B
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_EXTENDED_ENROLLMENT_STATUS
- ponteiro de estrutura de PWINBIO_EXTENDED_ENROLLMENT_STATUS Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_STATUS
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16ab3736e3ad5b0bcf10bed1fb606d3e6283715a6b10c44dcb4923920597d5e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910441"
---
# <a name="winbio_extended_enrollment_status-structure"></a>\_Estrutura de \_ status de registro ESTENDIdo WINBIO \_

Contém informações adicionais sobre o status de um registro em andamento.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_STATUS {
  HRESULT                  TemplateStatus;
  WINBIO_REJECT_DETAIL     RejectDetail;
  ULONG                    PercentComplete;
  WINBIO_BIOMETRIC_TYPE    Factor;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
  union {
    ULONG32 Null;
    struct {
      RECT BoundingBox;
      LONG Distance;
    } FacialFeatures;
    struct {
      ULONG GeneralSamples;
      ULONG Center;
      ULONG TopEdge;
      ULONG BottomEdge;
      ULONG LeftEdge;
      ULONG RightEdge;
    } Fingerprint;
    struct {
      RECT  EyeBoundingBox_1;
      RECT  EyeBoundingBox_2;
      POINT PupilCenter_1;
      POINT PupilCenter_2;
      LONG  Distance;
    } Iris;
    struct {
      ULONG32 Reserved;
    } Voice;
  } Specific;
} WINBIO_EXTENDED_ENROLLMENT_STATUS, *PWINBIO_EXTENDED_ENROLLMENT_STATUS;
```



## <a name="members"></a>Membros

<dl> <dt>

**TemplateStatus**
</dt> <dd>

O status da coleção de exemplo para o modelo de registro. Os valores a seguir são possíveis para esse membro.



| Valor                                                                                                                                                                                                  | Significado                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="S_OK"></span><span id="s_ok"></span><dl> <dt>**S \_ OK**</dt> </dl>                                                                     | O registro está pronto para ser salvo.<br/>                |
| <span id="WINBIO_E_INVALID_OPERATION"></span><span id="winbio_e_invalid_operation"></span><dl> <dt>**WINBIO \_ E \_ operação inválida \_**</dt> </dl> | Nenhum registro está em andamento.<br/>                       |
| <span id="WINBIO_I_MORE_DATA"></span><span id="winbio_i_more_data"></span><dl> <dt>**WINBIO \_ \_ mais \_ dados**</dt> </dl>                         | Mais exemplos são necessários para concluir o modelo.<br/> |
| <span id="WINBIO_E_BAD_CAPTURE"></span><span id="winbio_e_bad_capture"></span><dl> <dt>**\_captura WINBIO E \_ inadequada \_**</dt> </dl>                   | O exemplo mais recente não é utilizável.<br/>               |



 

</dd> <dt>

**RejectDetail**
</dt> <dd>

O motivo pelo qual o exemplo mais recente é inutilizável, se o valor do membro **TemplateStatus** for **WINBIO \_ E uma \_ \_ captura inadequada**.

</dd> <dt>

**PercentComplete**
</dt> <dd>

A melhor estimativa do adaptador do mecanismo para a porcentagem do modelo concluído, como um valor de 0 a 100.

</dd> <dt>

**Fator**
</dt> <dd>

O tipo de unidade biométrica para o qual essa estrutura contém informações sobre recursos e requisitos de registro do adaptador do mecanismo. Por exemplo, se o valor do membro **factor** for **WINBIO \_ tipo \_ impressão digital**, a estrutura de [**\_ \_ \_ informações do mecanismo estendido WINBIO**](winbio-extended-engine-info.md) se aplicará a um leitor de impressão digital e conterá as informações relevantes na estrutura **específico. FINGERPRINT** .

</dd> <dt>

**Subfator**
</dt> <dd>

Um valor de **\_ \_ subtipo biométrico WINBIO** que fornece informações adicionais sobre o registro.

</dd> <dt>

**Determinados**
</dt> <dd>

Informações sobre o status de um registro que está em andamento para um fator biométrico específico.

<dl> <dt>

**Nulo**
</dt> <dd>

Reservado. Deve ser zero.

</dd> <dt>

**FacialFeatures**
</dt> <dd>

Informações sobre o status de um registro que está em andamento para os recursos faciais.

<dl> <dt>

**BoundingBox**
</dt> <dd>

A posição dentro do quadro da câmera da face do indivíduo a ser registrado, em pixels. O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição. Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera. Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.

</dd> <dt>

**Alcance**
</dt> <dd>

A distância entre o local real da face e a distância focal ideal para a face. Esse valor varia de-100 a 100. 0 indica a distância ideal, os valores positivos indicam que o local real da face está muito distante, e os valores negativos indicam que o local real está muito próximo.

</dd> </dl> </dd> <dt>

**Fingerprint**
</dt> <dd>

Informações sobre o status de um registro em andamento para padrões de impressão digital.

<dl> <dt>

**GeneralSamples**
</dt> <dd>

O número total de amostras necessárias para criar um novo modelo de impressão digital.

</dd> <dt>

**Centraliza**
</dt> <dd>

O número de amostras para o centro da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**TopEdge**
</dt> <dd>

O número de amostras para a borda superior da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**BottomEdge**
</dt> <dd>

O número de amostras para a borda inferior da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**LeftEdge**
</dt> <dd>

O número de amostras para a borda esquerda da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> <dt>

**RightEdge**
</dt> <dd>

O número de amostras para a borda direita da impressão digital necessária para criar um novo modelo de impressão digital.

</dd> </dl> </dd> <dt>

**Iris**
</dt> <dd>

Informações sobre o status de um registro que está em andamento para padrões de íris.

<dl> <dt>

**EyeBoundingBox \_ 1**
</dt> <dd>

A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels. Se o sistema de reconhecimento de íris estiver monitorando apenas um olho, essa posição será da íris desse olho. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será da íris do olho no quadro da câmera. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho correto do indivíduo.

O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição. Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera. Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.

</dd> <dt>

**EyeBoundingBox \_ 2**
</dt> <dd>

A posição dentro do quadro da câmera de uma das íris do indivíduo a ser registrado, em pixels. Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio. Se o sistema de reconhecimento de íris estiver monitorando os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será a íris do olho à esquerda do indivíduo.

O tamanho do quadro da câmera determina o limite superior do número de pixels para essa posição. Obtenha a propriedade de **\_ \_ \_ \_ informações do sensor estendido da propriedade WINBIO** para determinar o tamanho do quadro da câmera. Um cliente que usa o monitor de presença deve executar a operação de dimensionamento para mapear a posição para o quadro da câmera.

</dd> <dt>

**PupilCenter \_ 1**
</dt> <dd>

A posição do centro de um dos Pupils do indivíduo a ser registrado. Se o sistema de reconhecimento de íris estiver monitorando apenas um dos olhos, essa posição será do centro da pupilidade desse olho. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos, mas apenas um olho estiver no quadro da câmera, essa posição será do centro da Pupil do olho no quadro da câmera. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro do Pupil do lado direito do indivíduo.

</dd> <dt>

**PupilCenter \_ 2**
</dt> <dd>

A posição do centro de um dos Pupils do indivíduo a ser registrado. Se o sistema de reconhecimento de íris estiver monitorando apenas um olho ou se apenas um olho estiver no quadro da câmera, esse valor estará vazio. Se o sistema de reconhecimento de íris estiver monitorando ambos os olhos e os dois olhos estiverem no quadro da câmera, essa posição provavelmente será do centro dos Pupil do lado esquerdo do indivíduo.

</dd> <dt>

**Alcance**
</dt> <dd>

A distância entre o local real da íris e a distância focal ideal para a íris. Esse valor varia de-100 a 100. 0 indica a distância ideal, os valores positivos indicam que o local real da íris está muito distante, e os valores negativos indicam que o local real está muito próximo.

</dd> </dl> </dd> <dt>

**Voz**
</dt> <dd>

Informações sobre o status de um registro que está em andamento para padrões de voz.

<dl> <dt>

**Reserved**
</dt> <dd>

Reservado.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                                                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                                                                                                     |
| parâmetro<br/>                   | <dl> <dt>Winbio \_ types.h (inclua Winbio.h para aplicativos cliente ou \_ adaptadores Winbio.h para adaptadores)</dt> </dl> |



 

 





