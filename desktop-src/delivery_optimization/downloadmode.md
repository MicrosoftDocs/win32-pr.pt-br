---
title: Enumeração de downloadmode (Deliveryoptimization. h)
description: Define os diferentes modos de download que a otimização de entrega usa.
ms.assetid: 7E9407C6-A22F-459E-B316-5E7809F0067A
keywords:
- Ignore a Otimização de Entrega e use o BITS. Por exemplo, selecione esse modo para que os clientes possam usar o BranchCache. enumeração
topic_type:
- apiref
api_name:
- DownloadMode
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ea753ef47dc2e6655d7e707466d7b0448bee7bec1f090b1baf4de04799283d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543720"
---
# <a name="downloadmode-enumeration"></a>Enumeração de downloadmode

Define os diferentes modos de download que a otimização de entrega usa.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DownloadMode { 
  DownloadMode_CdnOnly   = 0,
  DownloadMode_Lan       = 1,
  DownloadMode_Group     = 2,
  DownloadMode_Internet  = 3,
  DownloadMode_Simple    = 99,
  DownloadMode_Bypass    = 100
} DownloadMode;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DownloadMode_CdnOnly"></span><span id="downloadmode_cdnonly"></span><span id="DOWNLOADMODE_CDNONLY"></span>**DownloadMode_CdnOnly**
</dt> <dd>

Essa configuração desabilita o cache ponto a ponto, mas ainda permite que a otimização de entrega Baixe conteúdo de servidores da Microsoft. Esse modo usa metadados adicionais fornecidos pelos serviços de nuvem da Otimização de Entrega para oferecer uma experiência de download poderosa, confiável e eficientes.

</dd> <dt>

<span id="DownloadMode_Lan"></span><span id="downloadmode_lan"></span><span id="DOWNLOADMODE_LAN"></span>**DownloadMode_Lan**
</dt> <dd>

Esse modo de operação padrão para Otimização de Entrega permite que o compartilhamento ponto a ponto na mesma rede.

</dd> <dt>

<span id="DownloadMode_Group"></span><span id="downloadmode_group"></span><span id="DOWNLOADMODE_GROUP"></span>**DownloadMode_Group**
</dt> <dd>

quando o modo de grupo é definido, o grupo é selecionado automaticamente com base no site do Active Directory Domain Services do dispositivo (AD DS) (Windows 10, versão 1607) ou no domínio no qual o dispositivo é autenticado (Windows 10, versão 1511). No modo de grupo, o emparelhamento ocorre em sub-redes internas, entre dispositivos que pertencem ao mesmo grupo, incluindo dispositivos em escritórios remotos. Você pode usar a opção GroupID para criar seu próprio grupo personalizado independentemente domínios e sites do AD DS. O modo de download de grupo é a opção recomendada para a maioria das organizações que desejam obter a melhor otimização de largura de banda com a Otimização de Entrega.

</dd> <dt>

<span id="DownloadMode_Internet"></span><span id="downloadmode_internet"></span><span id="DOWNLOADMODE_INTERNET"></span>**DownloadMode_Internet**
</dt> <dd>

Habilite fontes de emparelhamento da Internet para Otimização de Entrega.

</dd> <dt>

<span id="DownloadMode_Simple"></span><span id="downloadmode_simple"></span><span id="DOWNLOADMODE_SIMPLE"></span>**DownloadMode_Simple**
</dt> <dd>

O modo Simples desabilita o uso dos serviços de nuvem de Otimização de Entrega completamente (para ambientes offline). A Otimização de Entrega alterna para esse modo automaticamente quando os serviços de nuvem de Otimização de Entrega não estão disponíveis ou acessíveis ou quando o tamanho do arquivo de conteúdo é menor que 10 MB. Nesse modo, a Otimização de Entrega fornece uma experiência de download confiável, sem cache ponto a ponto.

</dd> <dt>

<span id="DownloadMode_Bypass"></span><span id="downloadmode_bypass"></span><span id="DOWNLOADMODE_BYPASS"></span>**DownloadMode_Bypass**
</dt> <dd>

Ignore a Otimização de Entrega e use o BITS. Por exemplo, selecione esse modo para que os clientes possam usar o BranchCache.

</dd> </dl>

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------|----------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>      |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>  |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>               |
