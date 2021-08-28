---
description: A estrutura EXPERTENUMINFO fornece informações sobre o especialista.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Estrutura EXPERTENUMINFO (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 46942f1140cbb5f74685b16e468b68b85221deceeae2509a9d0676261898e238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118939033"
---
# <a name="expertenuminfo-structure"></a>Estrutura EXPERTENUMINFO

A **estrutura EXPERTENUMINFO** fornece informações sobre o especialista. Monitor de Rede aloca memória para a estrutura e a passa para o especialista quando chama a [**função Registrar Especialista.**](register-expert.md) Quando o especialista recebe a estrutura, ele deve preencher todas as informações que Monitor de Rede solicitações.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Szname**
</dt> <dd>

Nome do especialista.

</dd> <dt>

**szVendor**
</dt> <dd>

Nome do fornecedor que cria o especialista.

</dd> <dt>

**szDescription**
</dt> <dd>

Descrição do especialista. O valor do membro **szDescription** pode ser **NULL.** Se o nome for muito longo, ele será truncado na configuração padrão do visualizador.

</dd> <dt>

**Versão**
</dt> <dd>

O valor deve ser zero.

</dd> <dt>

**Sinalizadores**
</dt> <dd>

Os sinalizadores a seguir descrevem o especialista.



| Valor                                                                                                                                                                                                                                                    | Significado                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**SINALIZADOR \_ DE ENUM \_ ESPECIALISTA \_ CONFIGURÁVEL**</dt> </dl>                                          | O especialista dá suporte a chamadas para o [**método Configure.**](configure.md) <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**VISUALIZADOR \_ DE SINALIZADORES DE ENUM \_ ESPECIALISTA \_ \_ PRIVADO**</dt> </dl>                                   | O especialista requer uma conta privada (não compartilhada) Visualizador de Eventos. <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**SINALIZADOR \_ DE ENUM \_ ESPECIALISTA SEM \_ \_ VISUALIZADOR**</dt> </dl>                                                  | O especialista não envia notificações de eventos. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**SINALIZADOR \_ DE ENUM \_ ESPECIALISTA \_ \_ ADICIONE-ME \_ AO \_ RMC EM \_ \_ RESUMO**</dt> </dl> | Quando o foco está no painel de resumo, o especialista aparece no menu de contexto. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**SINALIZADOR \_ DE ENUM \_ ESPECIALISTA \_ \_ ADICIONE-ME \_ AO \_ RMC EM \_ \_ DETALHES**</dt> </dl>    | Quando o foco está no painel de detalhes, o especialista aparece no menu de contexto. <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

Lidar com o especialista. Quando a **estrutura EXPERTENUMINFO** é usada para registrar um especialista, o parâmetro é ignorado.

</dd> <dt>

**szDllName**
</dt> <dd>

Membro privado; não use.

</dd> <dt>

**Hmodule**
</dt> <dd>

Membro privado; não use.

</dd> <dt>

**pRegisterProc**
</dt> <dd>

Membro privado; não use.

</dd> <dt>

**pConfigProc**
</dt> <dd>

Membro privado; não use.

</dd> <dt>

**pRunProc**
</dt> <dd>

Membro privado; não use.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




