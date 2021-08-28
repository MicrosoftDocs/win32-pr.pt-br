---
title: Classe Win32 \_ InstalledProgramFramework
description: A classe Win32 InstalledProgramFramework representa uma estrutura de tecnologia em que uma instância do \_ Win32 InstalledWin32Program é compilada ou usa em \_ runtime.
ms.assetid: bb5c18c7-ec71-4579-8190-942de4fccd9e
keywords:
- Win32_InstalledProgramFramework classe Application and Device Inventory Provider
- Win32_InstalledProgramFramework classe Application and Device Inventory Provider , descrita
topic_type:
- apiref
api_name:
- Win32_InstalledProgramFramework
- Win32_InstalledProgramFramework.FrameworkName
- Win32_InstalledProgramFramework.FrameworkPublisher
- Win32_InstalledProgramFramework.FrameworkVersion
- Win32_InstalledProgramFramework.FrameworkVersionActual
- Win32_InstalledProgramFramework.ProgramId
- Win32_InstalledProgramFramework.IsPrivate
api_location:
- Root\CIMv2
api_type:
- Schema
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e447544dbfdebd6e4f4dd12752171089b8da041
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917864"
---
# <a name="win32_installedprogramframework-class"></a>Classe Win32 \_ InstalledProgramFramework

A **classe Win32 \_ InstalledProgramFramework** representa uma estrutura de tecnologia em que uma instância do [**Win32 \_ InstalledWin32Program**](win32-installedwin32program.md) é compilada ou usa em runtime. As estruturas que essa classe pode relatar atualmente são OpenSSL, Visual Basic, Visual C++ .Net, Visual C++, Java (detecta apenas os binários de runtime java) e CLR.

> [!Note]  
> O conjunto de estruturas que essa classe pode detectar pode ser atualizado ao longo do tempo.

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_InstalledProgramFramework
{
  string  FrameworkName;
  string  FrameworkPublisher;
  string  FrameworkVersion;
  string  FrameworkVersionActual;
  string  ProgramId;
  boolean IsPrivate;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ InstalledProgramFramework** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Win32 \_ InstalledProgramFramework** tem essas propriedades.

<dl> <dt>

**Frameworkname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

O nome da estrutura de que o aplicativo identificado por **ProgramId** depende.

</dd> <dt>

**FrameworkPublisher**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

O editor da estrutura.

</dd> <dt>

**FrameworkVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

A versão da estrutura em que o aplicativo tem uma dependência.

</dd> <dt>

**FrameworkVersionActual**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

A versão da estrutura que o aplicativo realmente usa em runtime, se a estrutura puder ser detectada.

</dd> <dt>

**Isprivate**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

TRUE se o aplicativo agrupar uma cópia privada da estrutura.

</dd> <dt>

**ProgramId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

O identificador exclusivo da [**instância Win32 \_ InstalledWin32Program,**](win32-installedwin32program.md) com a qual os dados da estrutura estão associados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



|                                     |                                                                                      |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                               |
| MOF<br/>                      | <dl> <dt>Aeinv.mof</dt> </dl> |



 

 





