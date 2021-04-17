---
description: A estrutura EXPERTENUMINFO fornece informações sobre o especialista.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Estrutura EXPERTENUMINFO (Netmon. h)
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
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783259"
---
# <a name="expertenuminfo-structure"></a>Estrutura EXPERTENUMINFO

A estrutura **EXPERTENUMINFO** fornece informações sobre o especialista. Monitor de Rede aloca memória para a estrutura e a transmite para o especialista ao chamar a função de especialista de [**registro**](register-expert.md) . Quando o especialista recebe a estrutura, ele deve preencher todas as informações que Monitor de Rede solicitações.

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

**szName**
</dt> <dd>

Nome do especialista.

</dd> <dt>

**szVendor**
</dt> <dd>

Nome do fornecedor que cria o especialista.

</dd> <dt>

**szDescription**
</dt> <dd>

Descrição do especialista. O valor do membro **szDescription** pode ser **nulo**. Se o nome for muito longo, ele será truncado na configuração do visualizador padrão.

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
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <dt>**sinalizador de enumeração de especialista \_ \_ \_ configurável**</dt> </dl>                                          | O especialista dá suporte a chamadas para o método [**Configure**](configure.md) . <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <dt>**Visualizador de sinalizador de enumeração de especialista \_ \_ \_ \_ privado**</dt> </dl>                                   | O especialista requer um Visualizador de Eventos privado (não compartilhado). <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <dt>**sinalizador de enumeração de especialistas \_ \_ \_ sem \_ Visualizador**</dt> </dl>                                                  | O especialista não envia notificações de eventos. <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <dt>**\_ \_ sinalizador de enumeração \_ de especialistas adicionar \_ -me \_ ao \_ RMC \_ no \_ Resumo**</dt> </dl> | Quando o foco está no painel Resumo, o especialista é exibido no menu de contexto. <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <dt>**\_sinalizador de enumeração \_ de especialista \_ \_ me adicionar \_ a \_ RMC \_ em \_ detalhes**</dt> </dl>    | Quando o foco está no painel de detalhes, o especialista é exibido no menu de contexto. <br/>  |



 

</dd> <dt>

**hExpert**
</dt> <dd>

Lide com o especialista. Quando a estrutura **EXPERTENUMINFO** é usada para registrar um especialista, o parâmetro é ignorado.

</dd> <dt>

**szDllName**
</dt> <dd>

Membro privado; Não use.

</dd> <dt>

**hModule**
</dt> <dd>

Membro privado; Não use.

</dd> <dt>

**pRegisterProc**
</dt> <dd>

Membro privado; Não use.

</dd> <dt>

**pConfigProc**
</dt> <dd>

Membro privado; Não use.

</dd> <dt>

**pRunProc**
</dt> <dd>

Membro privado; Não use.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




