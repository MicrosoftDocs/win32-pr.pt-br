---
description: Usado com a \_ propriedade de propriedade de política de IU NCRYPT \_ \_ para conter informações de interface de usuário para uma chave.
ms.assetid: c567d8ba-3315-4316-8e09-93b2c10a55ec
title: Estrutura de NCRYPT_UI_POLICY_BLOB ( \_ provedor de NCrypt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NCRYPT_UI_POLICY_BLOB
api_type:
- HeaderDef
api_location:
- Ncrypt_provider.h
ms.openlocfilehash: 21f9f6c0f6956ffa89da45c9dcd23727c0b3cea2d4f31131713f9ed5a0c3a2fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907596"
---
# <a name="ncrypt_ui_policy_blob-structure"></a>\_Estrutura de \_ blob de política de IU NCRYPT \_

A estrutura de **\_ blob de \_ política \_ de interface do usuário NCrypt** é usada com a propriedade de [**\_ propriedade de \_ diretiva \_ NCrypt UI**](key-storage-property-identifiers.md) para conter informações de interface de usuário para uma chave.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct __NCRYPT_UI_POLICY_BLOB {
  DWORD dwVersion;
  DWORD dwFlags;
  DWORD cbCreationTitle;
  DWORD cbFriendlyName;
  DWORD cbDescription;
} NCRYPT_UI_POLICY_BLOB;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

O número de versão da estrutura. Este membro deve conter 1.

</dd> <dt>

**dwFlags**
</dt> <dd>

Um conjunto de sinalizadores que fornecem informações ou requisitos adicionais da interface do usuário.



| Valor                                                                                                                                                                                                                                                                                                  | Significado                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span id="NCRYPT_UI_PROTECT_KEY_FLAG"></span><span id="ncrypt_ui_protect_key_flag"></span><dl> <dt>**NCRYPT \_ \_Sinalizador de \_ chave \_ de proteção de interface de usuário**</dt> <dt>0x00000001</dt> </dl>                                | Exiba a interface do usuário de chave forte, conforme necessário.<br/> |
| <span id="NCRYPT_UI_FORCE_HIGH_PROTECTION_FLAG"></span><span id="ncrypt_ui_force_high_protection_flag"></span><dl> <dt>**NCRYPT \_ \_Sinalizador de \_ alta \_ proteção \_ da força de interface do usuário**</dt> <dt>0x00000002</dt> </dl> | Force alta proteção.<br/>                           |



 

</dd> <dt>

**cbCreationTitle**
</dt> <dd>

O comprimento, em bytes, do título de criação. O título de criação é uma cadeia de caracteres Unicode terminada em nulo que especifica o texto que é usado como o título da caixa de diálogo de chave forte quando a chave é concluída. O título de criação deve ser colocado imediatamente após a estrutura de **\_ BLOB da \_ diretiva \_ de interface do usuário NCRYPT** . Se o valor do membro **cbCreationTitle** for definido como 0, um título de criação padrão será usado para o título da caixa de diálogo de chave forte. Esse membro só é usado na finalização de chave.

</dd> <dt>

**cbFriendlyName**
</dt> <dd>

O comprimento, em bytes, do nome amigável da chave. O nome amigável é uma cadeia de caracteres Unicode terminada em nulo que contém o texto que é exibido na caixa de diálogo chave forte como o nome da chave. O nome amigável deve ser colocado imediatamente após o título de criação neste BLOB. Se o valor do membro **cbFriendlyName** for definido como 0, um nome padrão será usado na caixa de diálogo chave forte. Esse membro é usado quando a chave é concluída e quando a chave é usada.

</dd> <dt>

**cbDescription**
</dt> <dd>

O comprimento, em bytes, da descrição da chave. A descrição da chave é uma cadeia de caracteres Unicode terminada em nulo que contém o texto que é exibido na caixa de diálogo chave forte como a descrição da chave. O valor da descrição deve ser colocado imediatamente após o nome amigável neste BLOB. Se o valor do membro **cbDescription** for definido como 0, uma descrição padrão será usada na caixa de diálogo chave forte. Esse membro é usado quando a chave é concluída e quando a chave é usada.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa estrutura está incluída no cabeçalho NCrypt \_ Provider. h. para usar a estrutura, você deve baixar o [Kit de desenvolvimento do provedor criptográfico](/collaborate/connect-redirect?InvitationID=CSDK-GYTG-R2PX&ProgramID=7264) do Microsoft Conexão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                          |
| parâmetro<br/>                   | <dl> <dt>NCrypt \_ Provider. h</dt> </dl> |



 

