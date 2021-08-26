---
description: A ação InstallAdminPackage copia o banco de dados do produto para o ponto de instalação administrativo, que é definido pela propriedade TARGETDIR.
ms.assetid: 9781f14b-0264-4d00-9a83-bd5400c614ec
title: Ação InstallAdminPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1879d711e1a52a7121326ba170bb3a004fbfb4ee988b35d19a16e1a53c3e2811
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996586"
---
# <a name="installadminpackage-action"></a>Ação InstallAdminPackage

A ação InstallAdminPackage copia o banco de dados do produto para o ponto de instalação administrativo, que é definido pela [**propriedade TARGETDIR.**](targetdir.md)

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                                 |
|-------|------------------------------------------------------------|
| \[1\] | Nome dos arquivos de instalação.                                     |
| \[6\] | Tamanho do banco de dados.                                          |
| \[9\] | Identificador do diretório de ponto de instalação administrativa. |



 

## <a name="remarks"></a>Comentários

A ação InstallAdminPackage também atualiza as informações resumidas do banco de dados e remove todos os arquivos de gabinete localizados em fluxos depois que o banco de dados é copiado.

 

 



